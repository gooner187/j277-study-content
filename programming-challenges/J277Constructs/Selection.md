# Selection

**Description:** Selection uses if, elif and else to make a program choose between different paths depending on whether a condition is True or False. It lets a program respond differently to different inputs.

## Example 1
```python
mark = 72
if mark >= 70:
    grade = "A"
elif mark >= 50:
    grade = "B"
else:
    grade = "C"
print(grade)
```

## Example 2
```python
age = 15
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

## Example 3
```python
temperature = 3
isRaining = True
if temperature < 5 and isRaining:
    print("Wear a coat and take an umbrella")
```
# Selection — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it displays "The sky is blue today". There is 1 error — check the indentation.
**Hint:** The print statement needs to be indented inside the if block. In Python, indentation shows what belongs inside a condition.

```python
skyColour = "blue"
if skyColour == "blue":
print ("The sky is blue today")
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it displays "The sky is NOT blue". There are 2 errors — check the order of the lines and the indentation of the else branch.
**Hint:** The variable must be declared before the if statement can use it. The else and its print must be on separate lines with correct indentation.

```python
if skyColour == "purple":
print ("The sky is blue today")
skyColour = "blue"
else:print("The sky is NOT blue")
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so that entering 2 displays "You entered a 2", entering 3 displays "You entered a 3" and anything else displays "You entered a 4". There are 4 errors — check the order and indentation.
**Hint:** The input must come before the if statement. Every print inside an if, elif or else needs to be indented.

```python
if numEntered == 2:
print("You entered a 2")
elif numEntered == 3:
print("You entered a 3")
else:
    print("You entered a 4")
numEntered = int(input("Enter a 2, 3 or 4"))
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so that entering a number displays the correct message — 5 or less, exactly 6, or anything above 6 shows "Wow!". There are 4 errors — check the order and indentation.
**Hint:** The input must be the first line. Every print inside the if, elif and else needs to be indented. The input line should not be in the middle of the selection block.

```python
if litter <=5:
print("5 or less is a good size")
elif litter == 6:
litter= int(input("How many puppies were born?"))
print("6 is manageable")
else:
print("Wow!")
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code for a taxi/coach company. Entering 4 or fewer passengers should send a 4-seater car, 5 to 16 should send a 16-seater, and 17 or more should send a coach. There are 4 errors — syntax, order, indentation and logic.
**Hint:** The input must come first. There is a missing colon on the first if line. Check the indentation of the print statements. Also check which vehicle is sent for which number of passengers — are the right messages in the right branches?

```python
if passengers <=4
    print("send coach")
elif passengers >4 and passengers <17:
print("send 16-seater")
else:print("send 4-seater car")
passengers= int(input("How many passengers?"))
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the cinema entry code. Age and ticket are already set. A customer aged 15 or over AND with a ticket should see "Please find your seat", otherwise "You are not allowed this time". There are 4 errors — syntax, boolean operator, comparison operator and indentation.
**Hint:** Check the boolean operator — do you need both conditions to be true, or just one? Check the comparison operator used with ticket. Look for missing colons. Fix the indentation of both print statements.

```python
age = 13
ticket = True
print("Welcome to the cinema")
print("This movie is rated 15")
print("")
print("You are not allowed this time")
if age >= 15 or ticket = True
print("Please find your seat")
else
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** Improve the code from Challenge 6. Ask the user to enter their age as an integer. Ask them to enter y or n for whether they have a ticket. The movie is rated 15. If they are old enough AND have a ticket display "Please find your seat", otherwise display "You are not allowed this time".
**Hint:** Use int(input()) for age. Compare the ticket answer to "y" using ==. Combine both checks with and.

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Write a game menu. Display options: "Press 1 for 1-player, 2 for 2-player, 3 for online". Ask the user to enter a choice. If they enter 1, 2 or 3 display a matching message. If they enter anything else display "Invalid choice".
**Hint:** Use input() to get the choice. Use if, elif, elif, else for the four possible outcomes. Remember input() returns a string so compare to "1", "2", "3" — not integers.

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Write a club entry system. To get in, a person must be over 18 AND either have an invite OR be a member. Ask for their age, whether they have an invite (y/n) and whether they are a member (y/n). Display "Welcome to the club" or "Sorry, you cannot enter".
**Hint:** You need brackets to group the OR condition: age > 18 and (hasInvite == "y" or isMember == "y"). The brackets make sure both parts of AND are evaluated correctly.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Using a nested if statement, ask the user if they want a kebab — y or n. If they type "n" display "are you feeling ok?". If they type "y" ask "with chilli sauce?" — if they say "n" display "hmm", otherwise display "of course you want chilli sauce".
**Hint:** A nested if sits inside another if or else block. Make sure both levels are indented correctly. The second if/else is inside the first else block.
