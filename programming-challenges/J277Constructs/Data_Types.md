# Data Types

**Description:** A data type defines what kind of value a variable holds - integer, real (float), string or Boolean - and what can be done with it. Using the correct type matters, since mixing types incorrectly causes errors.

## Example 1
```python
name = "Zara"      # str
age = 15            # int
height = 1.62        # float (real)
isMember = True      # bool
print(type(age))
```

## Example 2
```python
a = 7          # int
b = 2.5        # float
c = a + b      # adding int + float gives float
print(c, type(c))
```

## Example 3
```python
isRaining = False        # bool
temperature = 14         # int
description = "cloudy"   # str
print(isRaining, temperature, description)
```
# Data Types — Challenges

## Challenge 1
**Type:** write
**Difficulty:** easy
**Task:** Run the code below. Before running, predict what each line will print and whether the result is an int, float, str or bool. Write your prediction as a comment next to each line.
**Hint:** Adding an int and a float gives a float. Using + with two strings joins them. A comparison like > always gives a bool.

```python
print(10 + 5)
print(10 + 5.0)
print("10" + "5")
print(10 > 5)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Each variable below has been given the wrong data type. Fix all 4 so that score is an int, price is a float, name is a string and isPass is a bool.
**Hint:** Integers have no decimal point. Floats have a decimal point. Strings use quotes. Booleans are True or False (capital T and F).

```python
score = "95"
price = 5
name = True
isPass = "True"
# When fixed, this code should work without errors:
print("Score + 10 =", score + 10)
print("Price x 2 =", price * 2.0)
print("Hello " + name)
print("Passed:", isPass)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "You are 16 years old" but crashes with a TypeError. Fix the 1 error — you cannot join a string and an integer directly.
**Hint:** You can only concatenate strings with strings. You need to convert age to a string before joining it.

```python
age = 16
print("You are " + age + " years old")
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** The code should calculate a BMI of 22.9 but crashes because height is the wrong data type. Fix the 1 error.
**Hint:** You cannot do arithmetic on a string. Check what data type height should be for the calculation to work.

```python
height = "1.75"
bmi = round(70 / height ** 2, 1)
print("BMI:", bmi)
```

## Challenge 5
**Type:** write
**Difficulty:** medium
**Task:** In Python, booleans are a subtype of integer — True equals 1 and False equals 0. Run this code and predict every output before running. Then write 2 more examples of your own.
**Hint:** Because True == 1 and False == 0, you can use them in arithmetic. Try True * 10 or False + 99.

```python
print(True + True)
print(True + False)
print(False + False)
print(True * 5)
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** The code should print "Total: £11.96" but crashes because price is stored as a string. Fix the 1 error so the calculation works correctly.
**Hint:** You cannot multiply a string by an integer. Price needs to be stored as a float so arithmetic can be done on it.

```python
price = "2.99"
qty = 4
print("Total: £" + str(price * qty))
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** Run the code and study the three outputs. Write a comment next to each line explaining the data type of the result and why it is different for each operator.
**Hint:** / always gives a float result. // gives an int (whole number only, remainder dropped). % gives the remainder as an int.

```python
a = 7
b = 2
print(a / b)
print(a // b)
print(a % b)
```

## Challenge 8
**Type:** debug
**Difficulty:** medium
**Task:** The code is meant to add two numbers together to get 8, but instead prints "53". Fix the 1 error.
**Hint:** When you use + with two strings, Python joins them together instead of adding them. What do you need to do to a and b before adding them?

```python
a = "5"
b = "3"
print(a + b)
```

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Create a student record using all four J277 data types. Declare: studentName (str), studentAge (int), avgGrade (float), isPassed (bool). Print all four on one line in this format: "Priya age 15 average 87.5 passed: True". Then change the values and run it again.
**Hint:** Use print() with multiple arguments separated by commas. Make sure each variable holds the correct data type — not everything in quotes.

## Challenge 10
**Type:** debug
**Difficulty:** hard
**Task:** The code should calculate a shopping total of £6.75 but crashes because discount is the wrong type. Fix the 1 error. quantity=3, price=2.50, discount="0.1". Note: round(total, 2) is used to round the answer to 2 decimal places — round(value, decimal_places) is a built-in Python function.
**Hint:** You cannot multiply a number by a string. discount needs to be a number before it can be used in the calculation. round(total, 2) means "round total to 2 decimal places".

```python
quantity = 3
price = 2.50
discount = "0.1"
total = quantity * price * (1 - discount)
print("Total: £", round(total, 2))
```
