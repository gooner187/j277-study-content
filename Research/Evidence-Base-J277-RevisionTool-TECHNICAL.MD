# Evidence Base — J277 Revision Tool — TECHNICAL

*Internal working document. For the version to share with students, parents and
colleagues, see the CUSTOMER FACING edition.*

A running record of the research behind the tool's design decisions.

**How to read this document.** Design choices are sorted into three honest tiers,
because not everything in the tool is research-driven and it would be misleading
to imply otherwise:

- **Tier 1 — Built on evidence.** The research came first and determined the
  design. If the evidence changed, the feature would change.
- **Tier 2 — Consistent with evidence.** Decided for practical or pedagogical
  reasons, but supported by research found afterwards.
- **Tier 3 — Judgement call.** Teacher experience, usability, or pragmatism.
  No strong evidence either way, or the evidence is contested.

Keeping the tiers separate matters: if this is ever shown to students, parents or
colleagues, the strong claims need to be defensible and the weak ones need to be
labelled as what they are.

**Read the UK evidence section too.** Most of the underlying research is American
and lab-based. UK evidence bodies reviewing the same territory are notably more
cautious about how much of it survives contact with a real classroom. That section
is a caveat on everything above it, not a separate topic.

---

## Tier 1 — Built on evidence

### 1.1 Mastery criterion: 3 correct answers per question
**Where:** MCQ self-test after each card. A question drops out of rotation only
after 3 correct answers; a wrong answer resets its streak to zero.

**Evidence:** Rawson & Dunlosky's work on retrieval practice criteria found a
clear step change between two and three correct recalls. In their paired-associate
experiments, one-week retention was roughly 48% for items practised to two correct
recalls, 68% for three, and 75% for four. Their explicit prescriptive conclusion
for students is to practise to an initial criterion of **3 correct recalls**, then
relearn 3 times at widely spaced intervals. Gains flatten after three, so the extra
time cost isn't repaid.

**Why it's Tier 1:** the number 3 in the code comes directly from this finding.
It is set as `MASTERY_CRITERION` so it can be changed if the evidence does.

> Rawson, K. A., & Dunlosky, J. (2011). Optimizing schedules of retrieval practice
> for durable and efficient learning: How much is enough? *Journal of Experimental
> Psychology: General*, 140(3), 283–302.
>
> Vaughn, K. E., Dunlosky, J., & Rawson, K. A. (2016). Effects of successive
> relearning on recall. *Memory & Cognition*.

---

### 1.2 Stopping after ~4 rounds rather than grinding on
**Where:** `MAX_ROUNDS` safety valve. If questions remain unmastered after four
passes, the session ends with an invitation to return in a day or two.

**Evidence:** relearning in a *later* session is far more efficient than pushing
harder in the current one — Rawson & Dunlosky report that less than two minutes
per concept was needed in the first relearning session, and less than a minute by
the fifth. They also found the incremental benefit diminishes across relearning
sessions. Grinding within one sitting is the expensive way to buy retention; a gap
is the cheap way.

**Why it's Tier 1:** the feature exists *because* of this finding. Without it the
natural design would have been "loop until everything is mastered", which the
evidence says is poor value and (in a classroom) demoralising.

> Rawson, K. A., & Dunlosky, J. (2022). Successive relearning: An underexplored
> but potent technique for obtaining and maintaining knowledge. *Current Directions
> in Psychological Science*, 31(4).

---

### 1.3 Restudy loop when the first pass is poor (<50%)
**Where:** after the first pass through the questions, a student scoring under half
is returned to the memorise screen to re-read their card before continuing.

**Evidence:** the successive-relearning protocol in the literature is retrieval
practice **with restudy** — items are practised *and restudied as needed* until
recalled. Testing without the restudy step just rehearses failure.

**Why it's Tier 1:** this is a direct implementation of the "restudy as needed"
half of the protocol, which the original design had omitted.

---

### 1.4 Timestamping every pill, for spaced review
**Where:** `j277_pill_history` records `firstWrittenAt`, `lastTestedAt` and
`masteredAt` per pill. Intended to drive "not revised since March" reporting.

**Evidence:** Cepeda et al. taught over 1,350 people a set of facts, reviewed after
gaps of up to 3.5 months, then tested up to a year later. Increasing the study gap
first improved and then gradually reduced final performance — there is an optimal
gap, and it scales with how long you need to remember. The optimum was around 20%
of the test delay for delays of a few weeks, falling to about 5–10% for a year.

**Practical reading for a GCSE:** with an exam months away, useful review gaps are
**days to weeks**, not hours. This is why the tool records *when* a topic was last
seen rather than only whether it was seen.

> Cepeda, N. J., Vul, E., Rohrer, D., Wixted, J. T., & Pashler, H. (2008). Spacing
> effects in learning: A temporal ridgeline of optimal retention. *Psychological
> Science*, 19(11), 1095–1102.
>
> Cepeda, N. J., Pashler, H., Vul, E., Wixted, J. T., & Rohrer, D. (2006).
> Distributed practice in verbal recall tasks: A review and quantitative synthesis.
> *Psychological Bulletin*, 132(3), 354–380.

---

## Tier 2 — Consistent with evidence

### 2.1 The whole tool is built around self-testing, not re-reading
**Where:** the entire card → memorise → MCQ loop.

**Evidence:** Dunlosky et al. reviewed ten common study techniques and rated only
two as **high utility**: *practice testing* and *distributed practice* — because
they work across ages, abilities and materials. Rated **low utility** were
summarisation, highlighting, keyword mnemonics, imagery for text, and **rereading**.

**Why this matters:** the tool's core loop is the two high-utility techniques
combined, and it deliberately offers no highlighting or re-reading features. That
alignment was not planned from the research at the outset — it emerged from
wanting students to make and test cards — but it lands in the right place.

> Dunlosky, J., Rawson, K. A., Marsh, E. J., Nathan, M. J., & Willingham, D. T.
> (2013). Improving students' learning with effective learning techniques.
> *Psychological Science in the Public Interest*, 14(1), 4–58.

---

### 2.2 Question on the front, answer on the back
**Where:** card-writing flow; MCQ free-text questions require recall, not just
recognition.

**Evidence:** formats that require *recall* from long-term memory are more
effective for retention than those requiring only *recognition*. The card format
enforces recall; the free-text MCQ format does too, which is why it was kept
alongside multiple choice rather than replaced by it.

---

### 2.3 Low-stakes quizzing with immediate feedback
**Where:** the MCQ engine after each card. Nothing is graded, nothing is reported
to anyone, questions can be retried, and every answer gets immediate correct/
incorrect feedback plus the right answer.

This is the single best-evidenced part of the tool for **this age group**, which
matters: much learning research is done on undergraduates in laboratories, whereas
the studies below were run on 11–18 year olds, in real classrooms, on their actual
course content, measured against their actual graded exams.

**The core finding — quizzing raises exam performance:**

- **8th-grade science.** McDaniel, Agarwal, Huelser, McDermott & Roediger gave
  students low-stakes multiple-choice quizzes with feedback, where some target
  content was quizzed and some wasn't. Quizzing produced **gains of between 13%
  and 25% on summative unit examinations**, and the benefits **persisted on
  cumulative semester and end-of-year exams** — not just the next test.

- **6th-grade social studies.** Roediger, Agarwal, McDaniel & McDermott ran three
  experiments where students took low-stakes multiple-choice quizzes on real course
  material. Quizzed items outperformed items that were merely presented twice, and
  the effect showed up on **both chapter exams and semester exams**. The dependent
  measures were the tests students were actually graded on.

- **Both question formats work.** McDermott, Agarwal, D'Antonio, Roediger &
  McDaniel found that **both multiple-choice and short-answer quizzes** enhanced
  later exam performance in middle and high school classes. This directly supports
  keeping both formats in the tool rather than simplifying to multiple choice alone.

**Why feedback specifically:** quizzing in these studies is quizzing *with*
feedback. Feedback lets a failed retrieval attempt become learning rather than a
rehearsed error — a real risk, since repeatedly retrieving a wrong answer can
strengthen the wrong memory. Feedback also improves students' **metacognitive
judgements** about what they do and don't know; repeated re-reading tends to
inflate confidence, whereas testing gives a more accurate picture. This is the
**illusion of competence** that makes highlighting and re-reading feel productive
while producing little (see 2.1).

**The "low-stakes" part isn't incidental — it appears to reduce anxiety.** A common
worry is that more quizzing means more stress. Agarwal, D'Antonio, Roediger,
McDermott & McDaniel surveyed **1,408 middle and high school students** (ages
11–18) who had taken part in year-long classroom retrieval-practice programmes:
**92% reported that retrieval practice helped them learn, and 72% reported it made
them less nervous for unit tests and exams.** The authors describe it as the first
study to examine retrieval practice and classroom test anxiety, and recommend
teachers use it *to reduce* anxiety as well as improve learning.

*Caveat worth stating:* that anxiety finding is **self-reported survey data**, not
a physiological or behavioural measure of anxiety. It is strong evidence about how
students experience regular low-stakes quizzing, and weaker evidence about anxiety
as a clinical construct. Worth citing as "students report feeling less nervous"
rather than "quizzing is proven to reduce anxiety."

**Design implications actually taken:**
- Scores are never graded or shown to anyone else.
- Questions can be attempted repeatedly without penalty (see 1.1).
- Feedback is immediate, and shows the correct answer on a miss.
- A poor first pass sends the student back to the card rather than marking them
  down (see 1.3).

**Why this stays Tier 2 rather than Tier 1:** the quizzing was built before this
research was consulted — it came from wanting students to test themselves on cards
they'd written. The evidence is Tier-1 strength; the *decision path* was Tier 2.
Keeping that distinction honest is the point of the tiering.

> McDaniel, M. A., Agarwal, P. K., Huelser, B. J., McDermott, K. B., & Roediger,
> H. L. (2011). Test-enhanced learning in a middle school science classroom: The
> effects of quiz frequency and placement. *Journal of Educational Psychology*,
> 103(2), 399–414.
>
> Roediger, H. L., Agarwal, P. K., McDaniel, M. A., & McDermott, K. B. (2011).
> Test-enhanced learning in the classroom: Long-term improvements from quizzing.
> *Journal of Experimental Psychology: Applied*, 17(4), 382–395.
>
> McDermott, K. B., Agarwal, P. K., D'Antonio, L., Roediger, H. L., & McDaniel,
> M. A. (2014). Both multiple-choice and short-answer quizzes enhance later exam
> performance in middle and high school classes. *Journal of Experimental
> Psychology: Applied*, 20(1), 3–21.
>
> Agarwal, P. K., D'Antonio, L., Roediger, H. L., McDermott, K. B., & McDaniel,
> M. A. (2014). Classroom-based programs of retrieval practice reduce middle school
> and high school students' test anxiety. *Journal of Applied Research in Memory
> and Cognition*, 3(3), 131–139.

---

### 2.4 Spacing across sessions, not just within one
**Where:** the "come back in a day or two" message; pill timestamps; the design
for review scheduling.

**Evidence:** distributed practice is one of the two high-utility techniques above;
Cepeda et al.'s meta-analysis of 254 studies found spaced practice beat massed
practice for long-term retention. Spacing decides *when* to study; retrieval decides
*how*. The tool now records the data needed to act on this.

### 2.5 The binary/hex games as procedural fluency practice
**Where:** five games unlocked via the dashboard — Binary Count, Binary Blitz,
Binary Addition, Binary Shifts, HexSmash. All drill J277 1.2.4 (binary and
hexadecimal representation).

**These are not "gamification" and should not be filed with it.** The gamification
research (see 3.4) concerns *motivation layers* — points and badges bolted onto
otherwise unchanged learning. In these games the retrieval **is** the game
mechanic: converting binary to denary under time pressure is retrieval practice
with a scoreboard, not a reward for doing something else.

**Why they earn a separate entry:** they do a job the revision cards structurally
cannot. Binary conversion is a **procedural** skill, not a declarative fact. A card
can state what a binary shift does; only repeated practice makes a student *fluent*
at performing one. This matters for exam performance in a specific way — a student
still laboriously working out that 1011 = 11 has spent their working memory on the
conversion and has none left for the question being asked. Building the sub-skill
to automaticity frees capacity for the actual problem.

**Evidence:** rests on the same retrieval-practice base as 2.1–2.3, plus the
cognitive-load argument that automating component skills frees working memory for
higher-order work. Timed drilling is appropriate *here* precisely because the goal
is speed and accuracy on a mechanical conversion — it would be the wrong tool for
conceptual material like "what does the MAR store", where speed pressure adds
nothing.

**Unlock levels — a design decision with a pedagogical cost (now fixed).**
Originally these ran from level 3 to level 36. Given the XP economy (one pill
session ≈ 205 XP; level 36 ≈ several subtopics of work), **HexSmash was effectively
unreachable** for content typically taught in the first term. The gating was
backwards relative to need: the student who most needs binary practice is the one
with the least XP.

Revised to front-load, following the skill dependency (count → convert →
add/shift → hex):

| Game | Level | XP | Roughly |
|---|---|---|---|
| Binary Count | 2 | 17 | during the first quiz |
| Binary Blitz | 4 | 154 | end of first pill |
| Binary Addition | 6 | 429 | ~2 pills |
| Binary Shifts | 8 | 840 | ~4 pills |
| HexSmash | 10 | 1,389 | ~7 pills |

Plus a **topic override**: any student who begins writing cards for 1.2 unlocks all
of these immediately, regardless of level. Need beats progression.

**The general principle worth keeping:** it is fine to lock *cosmetic* rewards
behind progression. Locking *curriculum content* behind it has a real cost, and
should be done only where the content genuinely depends on prior skill.

---

## Tier 3 — Judgement calls (no strong evidence, or contested)

Being explicit about these is the point of the tiering.

### 3.1 Handwriting the cards by hand, on physical index cards
**Status: contested — do not claim research backing for the handwriting itself.**

It is tempting to cite Mueller & Oppenheimer's well-known "the pen is mightier than
the keyboard" finding. **That would be overclaiming.** A direct replication by
Morehead, Dunlosky & Rawson found performance did not consistently differ between
longhand, laptop, and eWriter groups — and in one experiment, not even from a group
who took no notes at all. Their meta-analysis found small, non-significant effects
favouring longhand, and the authors conclude that deciding which method is superior
is premature.

**What *can* be defended:** the value is in *generating and testing* the material,
not in the ink. Physical cards are justified here on practical grounds — they can be
shuffled, sorted into "got it / not yet" piles, and used away from a screen — and on
the strength of retrieval practice (2.1, 2.2), not on handwriting per se.

> Morehead, K., Dunlosky, J., & Rawson, K. A. (2019). How much mightier is the pen
> than the keyboard for note-taking? A replication and extension of Mueller and
> Oppenheimer (2014). *Educational Psychology Review*, 31(3), 753–780.

### 3.2 Maximum 5 questions per physical card
Teacher judgement — cards get overcrowded and hard to read beyond that. No specific
evidence consulted. Plausibly relates to working-memory limits and card legibility,
but that would be a post-hoc rationalisation rather than a reason.

### 3.3 The 5-minute memorise timer
A round number chosen for classroom practicality, and skippable. Not derived from
evidence on optimal study duration. Worth revisiting if it proves too long or short
in practice.

### 3.4 Gamification: XP, ranks, badges and skins
**Scope note:** this entry covers the *motivation layer only* — experience points,
the 55 ranks, badges, and cosmetic backgrounds. The **games themselves have moved
to 2.5**, because they teach spec content rather than reward it, and the evidence
for them is substantially stronger.

**Status: mixed evidence, and weaker for retention than for engagement.**
Meta-analyses do find positive average effects on learning outcomes, but two
findings caution against filing gamification alongside retrieval practice and
spacing:

1. **Effects shrink as interventions lengthen.** Gamified interventions of 1–3
   months average around g = 0.906, while those running beyond a semester fall to
   about g = 0.392 — a pattern attributed to the **novelty effect**, where
   engagement spikes because something is new and then isn't sustained. A GCSE
   course runs on exactly the timescale where the effect decays.
2. **Heterogeneity is extreme** (I² approaching 99% in one meta-analysis), meaning
   results depend enormously on design and context. An average effect size across
   studies that inconsistent is a weak basis for prediction.

On long-term retention specifically — the outcome this tool cares about — effects
are reported as positive but variable, particularly where the game layer is
competitive or poorly aligned to the learning objectives.

**There is also a motivational risk** worth naming: extrinsic rewards can undermine
intrinsic interest in tasks students would otherwise do willingly.

**Why it's still in the tool:** it gets students to open it, and a tool nobody opens
has an effect size of zero. That is a legitimate reason. It is not, however, a
claim that XP helps anyone remember what a MAR does — and it should not be
presented to students or colleagues as an evidence-based *learning* feature.

> Sailer, M., & Homner, L. (2020). The gamification of learning: A meta-analysis.
> *Educational Psychology Review*, 32, 77–112.
>
> Huang, R., et al. Meta-analytic work on gamification duration and novelty effects
> in educational contexts.

### 3.5 Abbreviations not accepted as free-text answers
Exam-technique judgement: OCR mark schemes generally expect full terms, so accepting
"MAR" would train a habit that loses marks. Grounded in exam experience, not research.

### 3.6 Spec as the single source of truth over textbooks
Curriculum-fidelity judgement, not a learning-science claim.

### 3.7 "Hinge questions" as the first card per spec bullet
The card-authoring framework opens each spec bullet with a broad hinge question
before the granular ones. The term comes from **UK formative assessment practice**
(most associated with Dylan Wiliam), where a hinge question is one whose answer
tells you whether a class is ready to move on.

**Status: borrowed concept, adapted.** In its original use a hinge question is a
*teacher's* diagnostic tool used live in a lesson to decide what to do next. Here
it's repurposed as a *student's* entry point into a topic — a related but different
job. Sound instinct, but the evidence for hinge questions as classroom diagnostics
doesn't automatically transfer to this use, so it sits in Tier 3.

> Wiliam, D. (2011). *Embedded Formative Assessment.* Solution Tree Press.

---

## UK evidence, and an important caveat

The studies in Tiers 1 and 2 are predominantly American. That doesn't invalidate
them, but UK evidence bodies have reviewed the same territory and reached a
**more cautious** conclusion about classroom application. Since this tool will be
used in an English secondary school, that caution belongs here — and it applies
across the whole document, not to any single feature.

### The EEF review (the key UK source)
The Education Endowment Foundation — the main evidence charity for schools in
England — commissioned a systematic review of cognitive science in the classroom,
covering spaced learning, interleaving, retrieval practice, cognitive load,
schemas, dual coding and embodied learning.

**What it found:** cognitive science principles *can* improve learning, and the
review recommends teachers have a working knowledge of them. **But** it flags real
limits: positive results often come from small or tightly controlled studies, and
we don't yet know how well the approaches work in everyday classroom conditions.
Put more bluntly by the review's lead author: laboratory and controlled-classroom
studies produce positive, replicable results for retrieval, spacing and
interleaving — but **when tested in realistic classroom environments, the effects
are mixed and the effect sizes tend to be much smaller.**

**What this means for this tool:** the direction of travel is well supported;
the *size* of the benefit in a real Year 11 classroom is uncertain. Claims should
be framed as "this is built on well-evidenced principles", not "this will raise
grades by 13–25%" — even though that figure appears in the US classroom studies
at 2.3.

> Perry, T., Lea, R., Jørgensen, C. R., Cordingley, P., Shapiro, K., & Youdell, D.
> (2021). *Cognitive science approaches in the classroom: A review of the evidence.*
> London: Education Endowment Foundation.

### The gap that matters most for this tool
Reflecting on the same evidence base, Professor Rob Coe drew a distinction worth
taking seriously: there is a great deal of evidence that **retrieval practice can
aid learning**, and much less that **teachers can straightforwardly introduce it**
in their own classrooms. His specific criticism of the school-based studies is
pointed — they almost always use **questions written by the researchers, which are
often identical to the questions on the final test.**

**Why this is directly relevant here:** the MCQs in this tool are teacher-written
and are *not* identical to OCR exam questions. So the studies showing large gains
may overstate what happens when a student answers my questions and then sits a real
J277 paper. That transfer is an assumption, not a demonstrated result. It is
arguably the single biggest open question about whether this tool works — and it's
worth being upfront about rather than buried.

This is a reason to keep the MCQs **as close to OCR question style and command
words as possible**, so that what students practise resembles what they'll face.
It is also a reason to eventually check tool usage against real exam outcomes
(see the reporting design document).

### Avoiding the tick-box trap
The EEF has also cautioned against turning cognitive science into a mechanical
routine — the "start every lesson with a retrieval quiz" approach applied
identically everywhere. Retrieval in maths shouldn't look like retrieval in
history, and rigid whole-school rules tend to hollow the practice out.

**Relevance here:** this tool is optional, self-directed, and student-paced rather
than a mandated lesson-starter. That's a defensible position, but it also means
uptake is a real risk — a tool nobody opens has an effect size of zero.

### Policy context (England)
Cognitive science is embedded in English education policy — the Early Career
Framework (2019) includes explicit training in these principles, and EEF survey
data found over 85% of responding teachers considered strategies like retrieval
practice, spacing and interleaving central to their teaching. So this tool is
aligned with what English teachers are already being trained to do, which matters
for adoption by colleagues.

### Where UK and US evidence agree
Both traditions agree on the fundamentals, and the disagreement is about **effect
size in the wild**, not about direction:
- retrieval practice beats re-reading;
- spacing beats massing;
- feedback matters;
- students systematically misjudge which strategies work.

The honest summary is: **the principles are sound, the classroom effect is smaller
and more variable than the headline studies suggest, and implementation quality
matters more than the technique's name.**

---

*(Space for the books referenced — add author, title, and which decision each one
informs, so the link between reading and design stays visible.)*

| Book / source | Author | Informs which decision |
|---|---|---|
|  |  |  |

---

## Maintenance notes

- When a new feature is added, add it here **at the time**, in the correct tier.
  Retrofitting evidence to decisions already made is how Tier 3 quietly becomes
  Tier 1 without anyone noticing.
- If a claim is contested (like 3.1), say so plainly. A document that admits
  uncertainty is more credible than one that doesn't.
- Tunable constants currently in the code: `MASTERY_CRITERION` (3),
  `MAX_ROUNDS` (4), `CARD_CAP` (5), `MEMORISE_SECONDS` (300).
