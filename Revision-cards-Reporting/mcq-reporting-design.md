# MCQ Reporting — Design

Reporting on self-test results, for two audiences: the **student** (their own
history and weak spots) and the **teacher** (how the class is doing). Designed
now; the data model is built for Supabase, with localStorage as the interim
cache so nothing has to be torn up when the database arrives.

---

## 1. Why the current data can't support reporting

Today the quiz writes one flat object to localStorage:

```
j277_selftest_progress = { "1.1-08_q2": { "correct": true }, ... }
```

This keeps only the **latest** result per question. It has no student identity,
no timestamp, no record of separate attempts, and no concept of a test "run".
That's enough for a single "have I seen this?" check, but it can't answer any of
the questions real reporting needs:

- *the student:* "Am I improving? Which questions do I keep getting wrong?"
- *the teacher:* "Which questions does the class struggle with? Who needs help?"

Both need **history** (every attempt, over time) and, for the teacher, **identity**
(whose attempt). So the first job isn't a report — it's a better record.

---

## 2. The data model (Supabase)

Three tables. The design principle: record **events**, not just current state.
A report is then a query over events, and you can always compute "latest state"
from events but never the reverse.

### `students`
One row per student. Identity that a teacher's view can group by.

| column        | type        | notes                                         |
|---------------|-------------|-----------------------------------------------|
| id            | uuid (PK)   | the student                                   |
| display_name  | text        | e.g. initials or name, teacher-visible        |
| class_group   | text        | e.g. "Year 11 set 2" — lets a teacher filter  |
| created_at    | timestamptz |                                               |

### `selftest_runs`
One row per completed quiz (one memorise→test cycle).

| column       | type        | notes                                              |
|--------------|-------------|----------------------------------------------------|
| id           | uuid (PK)   | the run                                            |
| student_id   | uuid (FK)   | → students.id                                      |
| pill         | text        | which pill was tested, e.g. "Cache"                |
| subtopic     | text        | e.g. "1.1.2"                                        |
| scope        | text        | "card" or "all" (this card vs everything made)     |
| total        | int         | questions in the run                               |
| correct      | int         | how many right                                     |
| started_at   | timestamptz |                                                    |
| finished_at  | timestamptz | lets you spot abandoned runs                       |

### `selftest_answers`
One row per question answered — the grain everything else is built from.

| column       | type        | notes                                              |
|--------------|-------------|----------------------------------------------------|
| id           | uuid (PK)   |                                                    |
| run_id       | uuid (FK)   | → selftest_runs.id                                 |
| student_id   | uuid (FK)   | denormalised for fast per-student queries          |
| question_id  | text        | e.g. "1.1-08_q2"                                    |
| pill         | text        | the pill this question was tested under            |
| correct      | boolean     |                                                    |
| given_answer | text        | what they typed/picked (useful for free-text)      |
| answered_at  | timestamptz |                                                    |

**Why answer-level grain matters:** every report either audience wants is a
`GROUP BY` over this one table. Class-wide question difficulty is
`GROUP BY question_id`. A student's weak spots is
`WHERE student_id = ? GROUP BY question_id`. Improvement over time is ordering
runs by `finished_at`. Storing the finest grain once means never re-instrumenting
to answer a new question later.

---

## 3. Write path (how data gets in)

Unchanged flow, richer record. When a quiz finishes, instead of overwriting the
flat object, the tool:

1. inserts one `selftest_runs` row (pill, scope, total, correct, timestamps), and
2. inserts one `selftest_answers` row per question.

This runs through the existing `store` layer / award seam, so it's the same
write-through pattern already designed: localStorage immediately (offline, instant),
Supabase upsert alongside (persistence, cross-device, teacher visibility).
localStorage keeps a rolling cache of the student's own recent runs; the server
holds the full history and everyone else's.

**Interim (pre-Supabase):** the same two structures live in localStorage as
arrays (`j277_selftest_runs`, `j277_selftest_answers`) keyed by the device id.
The reports below all work off these arrays now, and switch to Supabase queries
later with no change to the report UI — only the data source swaps.

---

## 4. Student-facing report

Lives in the **dashboard's Reports tab** (already exists; this deepens it) and
optionally as a richer end-of-run screen.

### 4a. Fixing the end-of-run screen (the screenshot)
The current screen lists raw IDs ("Worth another look: 1.1-06_q1, 1.1-08_q2…"),
which mean nothing to a student. Replace with:

- **Score**, as now ("2 / 9") with the encouraging line.
- **Weak questions shown as the question text**, not the id — a student sees
  *"Which three factors affect CPU performance?"*, not `1.1-06_q1`. (The tool
  already has the question objects in memory at results time, so this is just
  showing `q.question` instead of `q.id`.)
- **A one-line trend** if they've tested this pill before: "Last time: 4/9 →
  now 2/9" or "Best so far: 6/9". Pulled from prior runs of the same pill.

### 4b. Reports tab (history view)
Per pill the student has tested:

- **Latest score** and **best score**.
- **Attempts count** and a small **trend** (spark line or just "4 → 6 → 7").
- **Sticky questions** — questions wrong on their *most recent* attempt,
  shown as question text, so revision has a target.

The existing Reports tab already groups by topic from the flat store; this
upgrades it to read runs (so it can show trend and attempts, not just a single
accuracy bar).

---

## 5. Teacher-facing report

This is the piece that genuinely needs Supabase — it aggregates across students,
which a per-device store can't do. A separate teacher view (its own page, behind
whatever light auth you choose), reading the same three tables.

### 5a. Question difficulty (the most actionable one)
`GROUP BY question_id` across all students:

- **% correct per question**, sorted worst-first.
- Surfaces "the whole class gets `1.1-08_q3` wrong" — which tells you what to
  reteach, and sometimes that a *question itself* is badly worded.
- Filterable by pill / subtopic / class group.

### 5b. Pill coverage & mastery
Per pill: how many students have tested it, average latest score, % who've
reached a mastery bar (say ≥80%). Shows which topics the class has and hasn't
consolidated.

### 5c. Per-student view
For a named student: pills tested, latest/best per pill, and their sticky
questions — so a 1:1 conversation has data behind it. This is 4b, viewed by the
teacher.

### 5d. Class overview
Counts that make the dashboard feel alive: active students this week, runs
completed, most-tested pill, hardest question right now.

---

## 6. Privacy / safeguarding notes

Because this becomes student data on a server, a few things to decide before it
ships (flagging, not prescribing):

- **What identifies a student** — initials + class is lighter-touch than full
  names; enough for you to know who's who without storing more than needed.
- **Retention** — how long results are kept; a wipe at year-end is reasonable.
- **Access** — the teacher view needs to be behind auth so it isn't world-readable
  (Supabase row-level security handles this: students read only their own rows,
  the teacher role reads the class).

None of this blocks the build; it's the kind of thing worth settling once, early,
rather than retrofitting.

---

## 7. Build order (when Supabase is ready)

1. **Create the three tables** + row-level security.
2. **Switch the write path** — quiz completion writes runs + answers through the
   `store` layer (localStorage + Supabase). *This can happen now on localStorage
   alone*, so the history starts accumulating before the server exists.
3. **Upgrade the end-of-run screen** — question text instead of ids, plus the
   trend line. *Doable now.*
4. **Upgrade the Reports tab** — trend and attempts from runs. *Doable now on the
   local arrays.*
5. **Build the teacher view** — needs Supabase; build last.

**What's doable immediately** (items 2–4 on localStorage) gives the student-facing
half straight away and starts collecting the history the teacher view will need.
**What waits for Supabase** is only the cross-student aggregation (item 5) — which
is correct, because that's the part that fundamentally can't work per-device.
