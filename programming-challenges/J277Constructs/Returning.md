# Returning — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the function returns "Alex" and it is displayed. There are 3 errors — order, missing return keyword and the returned value not displayed.
**Hint:** The function must be defined before it is called. return sends a value back — check it is there. Wrap the function call in print() to display the returned value.

```python
print(getName())
def getName():
    "Alex"
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the function returns 16, it is stored in a variable and printed as "Age: 16". There are 3 errors — missing return, wrong variable name used in print and indentation.
**Hint:** The function needs a return statement. Check the variable name the result is stored in versus what is used in print. Fix the indentation of the return statement.

```python
def getAge():
return 16
age = getAge()
print("Age:", years)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the function returns double the number passed in and prints 14. There are 3 errors — missing colon, return uses wrong operator and result not displayed.
**Hint:** Doubling means multiplying by 2 not adding 2. Check the def line for a missing colon. Wrap the function call in print() to see the returned value.

```python
def double(n)
    return n + 2
double(7)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function returns 10 (the discount), it is used in a calculation and "Total: £ 70" is printed. There are 4 errors — missing colon, return missing, wrong operator in calculation and indentation.
**Hint:** Check the def line for a missing colon. The function needs a return statement. Subtracting a discount means using - not +. Fix the indentation inside the function.

```python
def getDiscount()
    10
price = 80
total = price + getDiscount()
print("Total: £", total)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the function so it returns the correct grade string for a score. 85 should return "Distinction", 55 "Merit" and 40 "Pass". There are 4 errors — missing colon, two wrong comparison operators and the results not displayed.
**Hint:** Check the def line for a missing colon. Distinction is 70 or above — check what operator and value is used. Merit starts at 50. Wrap all three calls in print() to display the returned strings.

```python
def gradeScore(score)
    if score > 70:
        return "Distinction"
    elif score > 50:
        return "Merit"
    else:
        return "Pass"
gradeScore(85)
gradeScore(55)
gradeScore(40)
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so getLength() and getWidth() each return a value which area() uses to calculate and return the area. For 8 and 5 it should print "Area: 40". There are 4 errors — missing returns in two functions, wrong operator in area and result not displayed.
**Hint:** Both getLength and getWidth need return statements. Area uses multiplication not addition. Wrap the area() call in print() with a label.

```python
def getLength():
    int(input("Enter length: "))
def getWidth():
    int(input("Enter width: "))
def area():
    return getLength() + getWidth()
print(area())
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function returns the sum of two numbers and prints "Sum: 20". There are 4 errors — missing colon, print inside function instead of return, wrong variable name used to store result and indentation.
**Hint:** A function that returns a value should use return not print inside. Check the def line for a missing colon. Check the variable name the result is stored in. Fix the indentation of the return line.

```python
def addNums(a, b)
    print(a + b)
answer = addNums(12, 8)
print("Sum:", total)
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Write a function called circleArea that takes one parameter r (radius) and returns the area rounded to 2 decimal places using PI * r * r. Declare PI = 3.141592653 before the function. Ask the user for a radius, call the function and print "Area:" followed by the result. For radius 5 the answer is 78.54.
**Hint:** Use round(PI * r * r, 2) in the return statement. Store the returned value in a variable before printing it with a label.

```python
PI = 3.141592653
```

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Write three functions: getPrice() that returns a float entered by the user, getVAT(price) that returns 20% of the price rounded to 2 decimal places, and totalPrice(price) that returns price plus the result of calling getVAT(price). Call getPrice(), store it, then print "VAT: £" and "Total: £" using the other two functions. For £50 the output is VAT: £10.0 and Total: £60.0.
**Hint:** getVAT returns price * 0.20 rounded to 2 decimal places. totalPrice calls getVAT inside it. Store the result of getPrice() once and pass it to both functions.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Write a function called highest that takes a list of numbers as a parameter. Inside, use a loop to find and return the highest value. Test it with scores = [45, 88, 72, 91, 63] — it should print "Highest score: 91".
**Hint:** Start by assuming the first item is the highest. Loop through the list — if any number is greater, update your highest variable. Return it after the loop. Pass the whole list as the argument when calling the function.

```python
scores = [45, 88, 72, 91, 63]
```
