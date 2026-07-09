# For Loop

**Description:** A for loop repeats a block of code a fixed, known number of times, often using range() to control how many times it runs. It suits tasks where the number of repetitions is known in advance.

## Example 1
```python
total = 0
for i in range(1, 6):   # runs 5 times: 1,2,3,4,5
    total = total + i
    print("Added", i)
print("Total:", total)
```

## Example 2
```python
colours = ["red", "green", "blue"]
for colour in colours:
    print("Colour:", colour)
```

## Example 3
```python
for i in range(2, 21, 2):     # even numbers from 2 to 20
    print(i)
```
# For Loop — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Rearrange the two lines of code to display the word "kebab" 10 times. You may also need to fix indentation.
**Hint:** The for loop must come before the print. The print needs to be indented inside the loop.

```python
print("kebab")
for i in range(10):
```

## Challenge 2
**Type:** extend
**Difficulty:** easy
**Task:** The code below displays answers to the 2 times table. Change it to display the 3 times table instead.
**Hint:** Look at the range() arguments — the step value controls what the table counts in. Also think about where the sequence should start and end.

```python
for i in range(0, 25, 2):
    print(i)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** The three lines of code are in the wrong order. Rearrange them so the program asks the user to enter their name and then displays it twice. Fix any indentation too.
**Hint:** You need to get the name before you can display it. The print must be inside the loop.

```python
print(name)
for i in range(2):
name = str(input("Input your name>>>"))
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** The lines of code are in the wrong order and there are 2 errors. Rearrange and fix so the program asks for a times table number and correctly displays all 12 answers. Fix any indentation too.
**Hint:** Input must come before the loop. Look carefully at every operator used — a times table means multiply, not add.

```python
for i in range(1,13):
number = int(input("Enter a times table: "))
print("showing the",number,"times table")
print(i ,"x", number, "=", i+number)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** The lines are in the wrong order and there are 2 errors. Rearrange and fix so the program counts down from 10 to 0 then displays "Blast off!". Fix any indentation too.
**Hint:** The for loop must come first. Check all three values inside range() carefully — start, stop and step all need to be correct for a countdown from 10 to 0.

```python
print (i)
print("!!Blast off!!")
for i in range(12, 3, -1):
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** The lines are in the wrong order and there are 2 errors. Fix and rearrange so the code displays each colour of the rainbow with its number. Expected output: "Colour 1 is red", "Colour 2 is orange" etc. Fix any indentation too.
**Hint:** number must be set to 0 before the loop. The counter should increase by 1 each time — check what number*2 does versus number. The for loop variable holds each colour.

```python
number = number + 1
number = 0
rainbow = ["red","orange","yellow","green","blue","indigo","violet"]
print("Colour", number*2, "is", i)
for i in rainbow:
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** Write a program that asks the user to enter an integer below 100. Use a for loop to display a backwards count from that number down to zero.
**Hint:** Use range() with three arguments — start, stop, step. A negative step counts downwards. Remember range() stops before the stop value.

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Lottery number generator. Import random on line 1. Use a for loop to generate and display 6 random integers between 0 and 50.
**Hint:** Use random.randint(0, 50) inside the loop. Your loop needs to run exactly 6 times.

```python
import random
```

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Monopoly money generator. Create an array called "money" with amounts ranging from 0 to 100000. Use a for loop to randomly assign and display a money amount to each of 8 players.
**Hint:** Use random.choice(money) to pick from the array. Your loop should run 8 times. Print something like "Player 1 gets £50000".

```python
import random
```

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Paint and decorating software. Ask "How many houses are booked in?" then for each house, ask how many walls need painting and what colour each wall is. Display all the answers.
**Hint:** You need a loop inside a loop — the outer loop goes through each house, the inner loop goes through each wall. This is called a nested loop.
