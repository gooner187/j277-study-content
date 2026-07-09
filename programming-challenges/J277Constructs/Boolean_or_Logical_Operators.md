# Boolean Operators

**Description:** Logical operators - and, or and not - combine or reverse Boolean conditions to build more complex logic. 'and' needs both sides True, 'or' needs only one side True, and 'not' reverses a Boolean value.

## Example 1
```python
age = 16
hasTicket = True
if age >= 12 and hasTicket:   # both must be True
    print("Entry allowed")
if not hasTicket:               # reverses the Boolean
    print("Buy a ticket")
```

## Example 2
```python
hasKey = False
hasCode = True
if hasKey or hasCode:      # only one needs to be True
    print("Door unlocked")
```

## Example 3
```python
age = 20
isMember = True
if age >= 18 and (isMember or age >= 21):
    print("Entry allowed")
```
# Boolean / Logical Operators — Challenges

## Challenge 1
**Type:** write
**Difficulty:** easy
**Task:** Run the code below. Before running, predict what each line will print. Write your prediction as a comment next to each line. The three operators are: and, or, not.
**Hint:** With AND, both sides must be True. With OR, only one side needs to be True. NOT flips the value.

```python
print(True and True)
print(True and False)
print(False and False)
```

## Challenge 2
**Type:** write
**Difficulty:** easy
**Task:** Run the code and predict the output before running. Then change all three lines so that every print displays False instead.
**Hint:** OR returns True if at least one side is True. Think about what combination of True/False would make OR return False.

```python
print(True or False)
print(False or False)
print(True or True)
```

## Challenge 3
**Type:** write
**Difficulty:** easy
**Task:** Run the code and predict the output before running. Then write two more examples of your own using not with a comparison expression.
**Hint:** not flips True to False and False to True. Try not (10 == 10) — what do you expect?

```python
print(not True)
print(not False)
print(not (5 > 3))
```

## Challenge 4
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "can enter" when age is 16 or over AND the person has a ticket. Fix the 2 operator errors so it works correctly.
**Hint:** Check the comparison operator for age — should it be > or >=? Check the comparison for hasTicket — is == the right operator here or should it just be the variable itself?

```python
age = 17
hasTicket = True
if age > 16 and hasTicket != True:
    print("can enter")
else:
    print("cannot enter")
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** The code should grant access if the password is correct AND the user is logged in, OR if they are an admin. Fix the 1 error — the logic is almost right but the brackets are in the wrong place.
**Hint:** Think about what should be grouped together. AND has higher priority than OR in Python, but brackets override this. What two things need to both be True together?

```python
password = True
loggedIn = False
isAdmin = True
if password and loggedIn or isAdmin:
    print("access granted")
else:
    print("access denied")
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** The code should print "door is open" when isLocked is True. Fix the 1 error — the not operator is missing or misplaced.
**Hint:** If isLocked is True, the door is locked not open. You need to check the opposite of isLocked to know if the door is open.

```python
isLocked = True
if isLocked:
    print("door is open")
else:
    print("door is locked")
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** A truth table shows all possible combinations of True/False for and, or and not. Complete the truth table by writing code that prints every row. There are 4 rows (True/True, True/False, False/True, False/False).
**Hint:** Use four separate if/print statements or a loop. Each row should show: A, B, A and B, A or B, not A.

## Challenge 8
**Type:** debug
**Difficulty:** medium
**Task:** The code should print "buy it" if stock is above 0 AND price is under 10, OR if there is a discount. There are 2 errors — fix the operators and brackets so the logic is correct.
**Hint:** Think about what needs to be grouped with AND first. Then OR combines that group with the discount check. Also check each comparison operator carefully.

```python
stock = 5
price = 8
discount = True
if stock > 0 or price < 10 and discount != True:
    print("buy it")
else:
    print("do not buy")
```

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Create a simple login system. Ask the user for a username and password. If username is "admin" AND password is "1234" print "logged in", otherwise print "access denied".
**Hint:** Use input() for both values. Use == to compare strings. Combine both checks with and.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** A nightclub entry system. A person is allowed entry if they are 18 or over, OR if they are 16 or over AND have parental consent, OR if they are a member of the club. Set age = 15, parentalConsent = True, memberOfClub = True. The output should be "allowed entry".
**Hint:** You need brackets to group the AND condition before combining with OR. Think: (condition1) or (condition2 and condition3) or condition4.

```python
age = 15
parentalConsent = True
memberOfClub = True
```
