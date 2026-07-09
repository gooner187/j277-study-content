# While Loop

**Description:** A while loop repeats a block of code for as long as a condition stays True, used when the number of repetitions is not known in advance. It must eventually make the condition False, or it never stops.

## Example
```python
count = 0
while count < 5:      # repeats while condition is True
    print("Count is", count)
    count = count + 1   # must change, or infinite loop!
print("Finished")
```

# While Loop — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Rearrange the four lines of code so the while loop keeps asking for a password until "kebab" is entered. Then it displays "correct password accepted". You may need to fix indentation.
**Hint:** The empty password must be declared first. The while condition needs to be checked before asking for input. The input line must be inside (indented under) the while loop.

```python
while password != "kebab":
password = ""
print("correct password accepted")
password = input('Please enter a password: ')
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Rearrange the five lines of code so the loop keeps displaying "Are we there yet?" and asking for a response until "y" is entered. Then it displays "Yay! We are there!!". You may need to fix indentation.
**Hint:** The answer variable must be declared before the while loop. The print and input lines must be inside the loop. The final print must be outside (after) the loop.

```python
answer = "N"
print("Yay! We are there!!")
answer = str(input("Please respond, y or n: ").upper())
print("Are we there yet?")
while answer != "Y":
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Rearrange the five lines of code so the loop keeps displaying the menu and asking for input until 2 is entered. Then it displays "Exited". You may need to fix indentation.
**Hint:** StayInLoop must be declared before the while. The print and input lines must be inside the loop. "Exited" must print after the loop ends.

```python
print("Exited")
StayInLoop = 1
print("Press 1 for choice or 2 to exit")
while StayInLoop != 2:
StayInLoop = int(input("Please respond, 1 or 2: "))
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** The code is meant to display "Loop 1" through to "Loop 10" then "End". There are 4 errors — fix them all.
**Hint:** loopCount must be declared before the while and without indentation. Only one "End" should print — after the loop. Check which lines need to be inside the loop.

```python
print("End")
loopCount = loopCount + 1
    loopCount = 1
while loopCount < 11:
print("Loop", loopCount)
loopCount = loopCount + 1
print("End")
```

## Challenge 5
**Type:** extend
**Difficulty:** easy
**Task:** The code keeps looping until a username is entered. Add one line of code after the while loop that displays the username followed by "accepted". For example: "Alex accepted".
**Hint:** Add the print statement after the while loop with no indentation. Use the username variable and join it with "accepted".

```python
username = ""
while not username:
    username = str(input("Enter username: "))
```

## Challenge 6
**Type:** extend
**Difficulty:** medium
**Task:** The code generates a random number and asks the user to guess it. At the moment it only asks once. Add one line of code (a while loop) to keep asking until the user guesses correctly. You may need to indent some lines.
**Hint:** The while condition should check if userGuess is not equal to number. The if/else block needs to be inside (indented under) the while loop.

```python
import random
number = random.randint(1,10)
userGuess = int(input("Guess the number between 1-10: "))
# Add one line of code here
if number < userGuess:
    userGuess = int(input("Too high, try again: "))
else:
    userGuess = int(input("Too low, try again: "))
print("Yay! You got it correct!!!")
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** The for loop version of a times table is shown and working. Below it is an unfinished while loop version with errors. Fix and complete the while loop version so it produces the same output.
**Hint:** The counter should start at 1 not 0. Fix the input prompt typo. Complete the print statement inside the loop. Add the missing line that increases the counter each time.

```python
# Working for loop version - study this first
number = int(input("Enter a times table: "))
for i in range(1, 13):
    print(i, "x", number, "=", i * number)
print("showing the", number, "times table")

# Fix and complete the while loop version below
timesTable = 0
UserChoice = int(input("Enter a times-ta: "))
while timesTable < 13:
    print(timesTable,
```

## Challenge 8
**Type:** extend
**Difficulty:** hard
**Task:** The code should ask the user to guess a random number but only give them 5 attempts. Fill in the 3 missing sections: the while loop condition (use "and"), the line that increases attempts, and the correct print for a right guess.
**Hint:** The while condition needs to check two things — the guess is wrong AND attempts is less than 5. Use and to combine them. The attempts line adds 1 each time. The correct guess message is "Yay! Correct guess".

```python
import random
number = random.randint(1, 10)
attempts = 0
guess = 0
# Add while loop condition here using "and"
    guess = int(input("Guess a number between 1 and 10: "))
    attempts = ### add 1 to attempts here ###
if guess == number:
    ### print correct message here ###
else:
    print("You are out of attempts")
```

## Challenge 9
**Type:** write
**Difficulty:** easy
**Task:** Use a while loop to display the numbers 0 to 10 on the screen, one per line.
**Hint:** Start a counter at 0. Use a while loop that runs while the counter is less than or equal to 10. Print the counter, then increase it by 1 each time.

## Challenge 10
**Type:** write
**Difficulty:** easy
**Task:** Write some code that repeatedly asks "What coding language is this?" and keeps asking until the user types "Python". When they type "Python" display "ok, thanks!".
**Hint:** Use a while loop with a condition that checks the answer is not equal to "Python". The message "ok, thanks!" should only print once, after the loop ends.
