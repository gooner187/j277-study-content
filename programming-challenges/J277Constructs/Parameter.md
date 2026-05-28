# Parameter — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure accepts a name as a parameter and prints "Hello Alex". There are 3 errors — order, missing parameter in the def line and indentation.
**Hint:** The procedure must be defined before it is called. The def line needs a parameter name inside the brackets. The print must be indented inside the procedure.

```python
greet("Alex")
def greet():
print("Hello", name)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure takes two parameters, adds them and prints the result. Calling addNums(5, 3) should print 8. There are 3 errors — a missing colon, wrong variable name inside and the result not being printed.
**Hint:** Check the def line for a missing colon. The parameter is called b but check what name is used inside the procedure. The print needs to be inside the procedure, not outside it.

```python
def addNums(a, b)
    print(a + c)
addNums(5, 3)
print(a + b)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure multiplies two numbers and prints 20. There are 3 errors — wrong number of arguments in the call, wrong operator and a missing parameter in the def line.
**Hint:** Count how many parameters are in the def line and how many arguments are passed in the call — they must match. Check the operator used. A parameter is missing from the def line.

```python
def multiply(x):
    print(x + y)
multiply(4, 5)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the procedure takes a name and age and prints "Welcome Sam you are 15 years old". There are 4 errors — wrong parameter names used inside, wrong argument order in the call, missing colon and indentation.
**Hint:** Check the parameter names declared in def versus what is used inside the print. The call passes arguments in order — make sure name and age match their parameter positions. Check for a missing colon.

```python
def welcome(name, age)
print("Welcome", firstName, "you are", years, "years old")
welcome(15, "Sam")
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the procedure checks an age parameter and prints "You can vote" if 18 or over, otherwise "Too young to vote". There are 4 errors — missing colon, wrong comparison, wrong parameter name used inside and indentation.
**Hint:** Check the def line for a missing colon. The parameter is called age — check what name is used in the if condition. >= means greater than or equal. Fix the indentation of both print statements.

```python
def checkAge(age)
    if years >= 18:
    print("You can vote")
    else:
    print("Too young to vote")
checkAge(20)
checkAge(15)
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function takes a name and an optional greeting parameter that defaults to "Hello". greetUser("Alex") should print "Hello Alex" and greetUser("Sam", "Hi") should print "Hi Sam". There are 3 errors — wrong default value position, wrong variable used inside and a missing colon.
**Hint:** The default parameter must come after the required one in the def line. Check what variable is used in the print — it should be name not userName. Check for a missing colon.

```python
def greetUser("Hello"=greeting, name)
    print(greeting, userName)
greetUser("Alex")
greetUser("Sam", "Hi")
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** Fix the function so it takes a parameter n, returns n squared and displays the result. Calling square(6) should print 36. There are 4 errors — missing colon, wrong calculation, result not stored and not printed.
**Hint:** Check the def line for a missing colon. Squaring means multiplying a number by itself. Store the return value in a variable. Print that variable.

```python
def square(n)
    return n + n
square(6)
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Write two procedures — areaRect(length, width) that prints the area, and perimRect(length, width) that prints the perimeter. Ask the user for a length and width, then call both procedures. For length=8, width=5 expected output is "Area: 40" and "Perimeter: 26".
**Hint:** Area = length * width. Perimeter = 2 * (length + width). Ask for both inputs before calling either procedure. Pass the same variables to both calls.

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Write a function called totalCost that takes two parameters: price (float) and qty (int). It should return price multiplied by qty. Ask the user for a price and quantity, call the function and print "Total: £" followed by the result rounded to 2 decimal places.
**Hint:** Use float(input()) for price and int(input()) for quantity. Return the result from the function. Use round(value, 2) when printing.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Write a procedure called bmi that takes two parameters: weight (kg) and height (m). Inside, calculate BMI using weight / (height * height) rounded to 1 decimal place. Use an if/elif/else to print the BMI and whether the person is "Underweight" (under 18.5), "Healthy weight" (under 25) or "Overweight". Call it three times: bmi(70, 1.75), bmi(50, 1.75) and bmi(100, 1.75).
**Hint:** Use round(weight / (height * height), 1) for the calculation. The three calls should produce: 22.9 Healthy weight, 16.3 Underweight, 32.7 Overweight.
