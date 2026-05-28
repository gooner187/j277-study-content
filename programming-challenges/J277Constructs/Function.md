# Function — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the three lines of code so the function is defined, returns a value and displays it correctly. It should print "Hello, world!". Check the order and indentation.
**Hint:** A function must be defined before it is called. The return statement must be indented inside the def block. Use print() around the function call to display the returned value.

```python
print(greeting())
def greeting():
return "Hello, world!"
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the function doubles a number and returns the result. Calling double(5) should print 10. There are 3 errors — a missing colon, a wrong operator and the return value not being printed.
**Hint:** Check the def line for a missing colon. The function should multiply by 2, not add 2. Wrap the function call in print() to display the returned value.

```python
def double(num)
    return num + 2
double(5)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the function adds two numbers and returns the result. It should print 10. There are 3 errors — a duplicate parameter name, the return value stored but not printed, and indentation.
**Hint:** Check the parameter names in the def line — are they both unique? The return statement needs to be indented. The stored result needs to be printed.

```python
def addNums(a, a):
return a + b
result = addNums(7, 3)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function returns the square of a number and the result is displayed. It should print "Square of 4 is 16". There are 4 errors — a missing colon, wrong calculation, wrong variable used in print and the return value not being captured.
**Hint:** Check for a missing colon. Squaring a number means multiplying it by itself, not adding. Store the return value in a variable before using it in print. Check the variable name used in the print statement.

```python
def squareNum(n)
    return n + n
print("Square of 4 is", n)
squareNum(4)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function joins a first and last name and returns the full name. It should print "Full name: Ada Lovelace". There are 4 errors — a missing space in the return, wrong variable name, wrong data type for input and the result not being stored before printing.
**Hint:** Check the return statement — is there a space between first and last? Check what variable name is used in the call. Should the inputs be int or str? Store the return value in a variable then print it.

```python
def fullName(first, last):
    return first + last
name = fullName(int(input("First name: ")), int(input("Last name: ")))
print("Full name:", fullname)
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function returns "Pass" if score is 50 or above and "Fail" otherwise. It should print "Pass" for 72 and "Fail" for 35. There are 4 errors — a missing colon, wrong comparison operator, missing return in else and the results not being printed.
**Hint:** Check the def line for a missing colon. >= means greater than or equal to — check what is used. The else branch also needs a return. Wrap both function calls in print().

```python
def passOrFail(score)
    if score > 50:
        return "Pass"
    else:
        "Fail"
passOrFail(72)
passOrFail(35)
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function calculates and returns the area of a circle. It should display "Area: 78.54" when radius is 5. There are 3 errors — wrong formula, missing round() and the result not being displayed.
**Hint:** The area formula is PI * radius * radius, not PI + radius. Use round(value, 2) to get 2 decimal places. Print the returned value with a label.

```python
PI = 3.141592653
def circleArea(radius):
    return PI + radius + radius
radius = float(input("Enter radius: "))
circleArea(radius)
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Write a function called celsiusToFahrenheit that takes one parameter called c and returns the temperature converted to Fahrenheit using the formula (c * 9/5) + 32. Ask the user for a temperature in Celsius and print the result. 100°C should give 212.0.
**Hint:** Return the result of the formula — don't print inside the function. Store the return value in a variable and then print it.

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Write a function called maxNum that takes two parameters a and b. It should return whichever is larger. Use an if/else inside the function. Test it by calling maxNum(8, 12) — it should return 12.
**Hint:** Use if a > b: return a, else: return b. The function returns a value — use print() around the call to display it.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Write a function called bmi that takes two parameters: weight (kg) and height (m). It should return the BMI rounded to 1 decimal place using the formula weight / (height * height). Ask the user for their weight and height, call the function, store the result and display it. Then use an if/elif/else to display whether they are "Underweight" (under 18.5), "Healthy weight" (under 25) or "Overweight".
**Hint:** Use float(input()) for both values. Return round(weight / (height * height), 1) from the function. The if/elif/else checking goes after the function call using the stored result.
