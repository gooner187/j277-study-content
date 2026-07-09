# Random

**Description:** The random module lets a program generate unpredictable values, such as a random integer between two numbers using randint() - useful for games, quizzes and simulations. It must be imported before use.

## Example
```python
import random                       # must import first

dice = random.randint(1, 6)        # random int 1 to 6
print("You rolled:", dice)

choice = random.choice(["Y", "N"])   # random pick from list
print(choice)
```

# Random — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it generates and displays a random integer between 0 and 10. There are 4 errors — a wrong import name, a wrong function name, wrong range values and a variable name typo.
**Hint:** The module is called random not randon. The function is randint not randinp. The range should start at 0 not 5. Check the variable name in print().

```python
import randon

number = random.randinp(5,10)
print(numbre)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it generates two random integers between 0 and 10, adds them together and displays the sum correctly e.g. "6 + 8 = 14". There are 5 errors — import typo, two module name typos, wrong operator and a variable name typo.
**Hint:** Check the import line and both uses of the module name. total should add num1 and num2 not subtract. Check the variable name in the final print.

```python
impert random

num1 = rendom.randint(0,10)
num2 = random.rondint(0,10)

total = num1 - num1

print(num1,"+",num2,"=",totol)
```

## Challenge 3
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so it generates a random times table (between 1 and 12) and displays all 12 answers. There are 8 errors — import typo, module name typos, missing bracket, missing colon, wrong bracket type on print, variable name typo and a missing comma.
**Hint:** Work through line by line — import, module name, closing bracket on randint, colon after for, print uses () not {}, check the variable name for number, and check all commas inside print.

```python
inport ramdam

number = rindom.randint(6,12

for i in range(1,13)
    print{i, "x", numbre, "=" i*number)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so it generates two random numbers between 1 and 12, multiplies them, asks the user the answer and checks if they are correct. There are 6 errors — import typo, module name typo, inconsistent variable name, wrong conversion function, variable name typo and missing colon.
**Hint:** Check the import and module name. total uses num2 but was it declared as num2 or number2? str() converts to string not strong(). Check tootal in the if condition. Check for a missing colon.

```python
import randoom

num1 = random.randint(1,12)
number2 = mandem.randint(1,12)

total = num1 * num2

num1 = str(num1)
num2 = strong(num2)

answer = int(input("What is "+num1+" x "+num2+">>>"))
if tootal == answer
    print("correct!")
else: print("incorrect!")
```

## Challenge 5
**Type:** debug
**Difficulty:** hard
**Task:** Fix the code so it asks 5 multiplication questions using random numbers, checks each answer and displays the final score out of 5. There are 7 errors — wrong range, incomplete randint, incomplete num2 assignment, input typo, variable name typo, wrong increment value and print typo.
**Hint:** The loop should run 5 times not 2. Complete the randint call for num2. Assign str(num2) to num2. Fix input spelling. Check the variable name in the if condition. Each correct answer adds 1 not 17. Fix the print in else.

```python
import random

correctAnswerCount = 0

for i in range(2)
    num1 = random.randint(1,12)
    num2 = random.rand

    total = num1 * num2

    num1 = str(num1)
    num2 =

    answer = int(inpot("What is "+num1+" x "+num2+">>>"))
    if totel == answer:
        print("correct!")
        correctAnswerCount = correctAnswerCount + 17
    
    else: prunt("incorrect!")

print("You got",correctAnswerCount,"/5")
```

## Challenge 6
**Type:** write
**Difficulty:** medium
**Task:** Write a dice roller. The code displays "Press spacebar then enter to roll, or x to exit". Use a while loop so it keeps rolling until the user types "x". Each roll generates a random number between 1 and 6 and displays it.
**Hint:** Use a while loop with a condition that checks the input is not "x". Use random.randint(1, 6) for the roll. Ask for input at the start of each loop iteration.

```python
import random
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** The lottery number generator is in the wrong order and has an extra duplicate line. Rearrange it so it generates 6 unique random numbers between 1 and 50, sorts them and displays them. Fix the indentation too.
**Hint:** Import first. Declare the empty list and the count variable before the while loop. The while loop body should only have the randint and one append — remove the duplicate. Sort and print come last.

```python
print("Your lottery numbers are:", lottery_numbers)

import random

        lottery_numbers.append(number)

while len(lottery_numbers) < num_lottery_numbers:
    number = random.randint(1, 50)
    if number not in lottery_numbers:
        lottery_numbers.append(number)

lottery_numbers.sort()
num_lottery_numbers = 6
lottery_numbers = []
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Create a "guess the number" game. Generate a random number between 1 and 5. Use a while loop so the user keeps guessing until correct. Display "too high" or "too low" for wrong guesses. When correct, display "It took you x guesses" where x is the number of attempts.
**Hint:** Use a counter variable starting at 0 and increment it each guess. The while condition checks if the guess is not equal to the number. Print the counter at the end.

```python
import random
```

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Create a magic 8-ball. Ask the user to type a yes/no question. Store 6 possible answers in a list e.g. "Yes", "No", "No chance", "One day", "Definitely", "Ask again later". Use random.choice() to pick and display one.
**Hint:** Declare a list of answer strings. Use random.choice(answers) to pick one randomly. The question the user types does not affect the answer — it is always random.

```python
import random
```

## Challenge 10
**Type:** extend
**Difficulty:** hard
**Task:** The code below randomly picks rock, paper or scissors. Extend it so the user enters their choice, the code compares both, displays who won and keeps score of wins for both user and computer across 3 rounds. Display the final scores at the end.
**Hint:** Use a for loop for 3 rounds. Store user wins and computer wins in variables. Compare choices using if/elif — remember rock beats scissors, scissors beats paper, paper beats rock. Print totals after the loop.

```python
import random

weapons = ["rock", "paper", "scissors"]
selected = random.choice(weapons)
print(selected)
```
