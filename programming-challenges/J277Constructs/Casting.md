# Casting

**Description:** Casting converts a value from one data type to another, such as turning text into an integer with int() or a number into text with str(). It matters because input() always returns a string, even for numbers.

## Example 1
```python
age = input("Enter your age: ")   # input() always gives a str
age = int(age)                       # cast str to int
nextYear = age + 1
print("Next year you'll be", nextYear)
```

## Example 2
```python
score = 95
print("Your score is " + str(score))   # cast int to str to join
```

## Example 3
```python
value = input("Enter a decimal number: ")
value = float(value)          # cast str to float
print(value * 2)
```
# Casting — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "Age: 17" but crashes with a TypeError. Fix the 1 error — you cannot join a string and an integer.
**Hint:** Use str() to convert the integer to a string before joining it with the rest of the message.

```python
age = 17
print("Age: " + age)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** The code should add two numbers to get 35 but instead prints "2510". Fix the 1 error.
**Hint:** num1 and num2 are strings. The + operator joins strings instead of adding them. Cast both to integers before adding.

```python
num1 = "25"
num2 = "10"
print(num1 + num2)
```

## Challenge 3
**Type:** write
**Difficulty:** easy
**Task:** Run the code and note the output. Then write a comment explaining why int(3.9) gives 3 and not 4. What is the difference between int() casting and round()?
**Hint:** int() does not round — it removes everything after the decimal point (truncation). round() rounds to the nearest whole number.

```python
pi = 3.14159
print(int(pi))
print(round(pi))
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** The code should calculate the average of 3 scores and display it as a float. Fix the 1 error so the result shows 78.33... instead of 78.
**Hint:** Dividing two integers gives a float in Python 3, but adding three integers gives an integer. Try casting one of the values before dividing.

```python
score1 = 75
score2 = 80
score3 = 80
average = score1 + score2 + score3 / 3
print(average)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** The code asks a user for a score and tries to add 10 to it but crashes with a TypeError. Fix the 1 error — input() always returns a string.
**Hint:** Cast the result of input() to an integer before using it in arithmetic.

```python
score = input("Enter your score: ")
total = score + 10
print("Total:", total)
```

## Challenge 6
**Type:** write
**Difficulty:** medium
**Task:** Run the code and predict every output before running. Then write a comment explaining the difference between int() casting and round() for each value shown.
**Hint:** int() truncates (removes the decimal part). round() rounds to the nearest integer. They give different results for values like 3.9 and 3.1.

```python
print(int(3.9))
print(round(3.9))
print(int(3.1))
print(round(3.1))
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** Run the code and predict every output before running. Then write a comment next to each line explaining why that value casts to True or False.
**Hint:** 0 and empty string "" cast to False. Any non-zero number or non-empty string casts to True.

```python
print(bool(0))
print(bool(1))
print(bool(""))
print(bool("hello"))
print(bool(-5))
```

## Challenge 8
**Type:** debug
**Difficulty:** medium
**Task:** The code should check if a temperature reading is above 37.5 and print "fever" or "normal". Fix the 1 error — the temperature value is stored as a string.
**Hint:** You cannot compare a string to a float using >. Cast temperature to a float before the comparison.

```python
temperature = "36.6"
if temperature > 37.5:
    print("fever")
else:
    print("normal")
```

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Write a program that asks the user to enter two numbers (they will come in as strings). Cast them both to floats, add them, multiply the result by 1.5, then cast the final answer to an int and display it.
**Hint:** Chain your casts step by step. Get input → cast to float → do arithmetic → cast to int → print.

## Challenge 10
**Type:** debug
**Difficulty:** hard
**Task:** The code should calculate the area and perimeter of a rectangle and display them, but crashes because length and width are strings. Fix the 2 errors. Expected output: "Area: 60" and "Perimeter: 34".
**Hint:** Cast length and width to integers before using them in calculations. You will need to cast in two places.

```python
length = "12"
width = "5"
area = length * width
perimeter = 2 * (length + width)
print("Area:", area)
print("Perimeter:", perimeter)
```
