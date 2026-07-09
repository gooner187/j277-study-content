# Argument

**Description:** An argument is the actual value sent into a function or procedure when it is called, matching the parameter in the definition. The parameter is the placeholder name; the argument is the real value supplied.

## Example
```python
def convertToPounds(pence):
    return pence / 100

print(convertToPounds(250))   # 250 is the argument
print(convertToPounds(99))     # 99 is a different argument
```

# Argument — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure receives "Alex" as an argument and prints "Hello Alex". There are 3 errors — order, the argument is missing from the call and indentation.
**Hint:** The procedure must be defined before it is called. The call needs an argument inside the brackets — the value to pass in. The print must be indented inside the procedure.

```python
greet()
def greet(name):
print("Hello", name)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure receives a number as an argument and prints double its value. Passing 5 should print 10. There are 3 errors — the argument is the wrong type, missing colon and the argument is missing from the call.
**Hint:** The argument "5" is a string — a number needs to be passed without quotes. Check the def line for a missing colon. The call needs an argument inside the brackets.

```python
def double(num)
    print(num * 2)
double("5")
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure receives one argument and prints "Name: Sam". There are 3 errors — too many arguments in the call, wrong variable used inside and indentation.
**Hint:** Count the parameters in the def line — the call must pass the same number of arguments. Check what variable name is used in the print versus what is declared as the parameter. Fix the indentation.

```python
def showName(name):
print("Name:", firstName)
showName("Sam", "Jones")
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the procedure prints "I am Alex and I am 15 years old". There are 4 errors — argument order in the call is wrong, wrong variable names used inside, missing colon and indentation.
**Hint:** Arguments are passed in the order they appear in the call. Check what the def line calls each parameter versus what is used inside the print. Fix the colon and indentation.

```python
def introduce(name, age)
print("I am", years, "and I am", firstName, "years old")
introduce(15, "Alex")
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so a variable is passed as an argument to the function and the result is printed. Entering 7 should print 49. There are 4 errors — missing colon, wrong operator, variable not passed as argument and result not printed.
**Hint:** Check the def line for a missing colon. Squaring means multiplying a number by itself. The variable userNum needs to be passed inside the brackets of the call. Wrap the call in print().

```python
def square(n)
    return n + n
userNum = int(input("Enter a number: "))
square()
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so an expression is passed as an argument and the result is printed. addTen(5 * 2) should print 20. There are 3 errors — missing colon, wrong operator inside the function and the result not displayed.
**Hint:** A mathematical expression can be used directly as an argument — the result is calculated first then passed in. Check the operator inside the function. Wrap the call in print().

```python
def addTen(n)
    return n - 10
print(addTen(5 + 2))
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the function is called twice with different arguments. area(8, 5) should print 40 and area(3, 3) should print 9. There are 4 errors — missing colon, wrong operator, wrong arguments in the second call and results not printed.
**Hint:** Area uses multiplication not addition. Check the def line for a missing colon. The second call has the wrong arguments — 3 times 3 should give 9. Wrap both calls in print().

```python
def area(l, w)
    return l + w
print(area(8, 5))
area(4, 2)
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Write a procedure called shout that takes one argument called word. Inside, print the word in uppercase followed by "!!!". Call it twice — once with "python" (prints "PYTHON!!!") and once with "hello" (prints "HELLO!!!").
**Hint:** Use word.upper() to convert to uppercase. Concatenate "!!!" using +. The argument changes each time you call the procedure.

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Write a procedure called canDrive that takes one argument called age. If age is 17 or over print "You can drive", otherwise print "You cannot drive yet". Call it twice — once with 18 and once with 15.
**Hint:** Use >= for the comparison. Each call passes a different argument — the same procedure handles both cases. No return value needed, just print inside.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Write two functions — getDiscount(price, percent) that returns the discount amount, and finalPrice(price, percent) that calls getDiscount and returns the final price rounded to 2 decimal places. Ask the user for a price and percentage, then print "Final price: £" followed by the result. For £80 at 20% the answer is £64.0.
**Hint:** getDiscount returns price * (percent / 100). finalPrice calls getDiscount, subtracts the result from price and rounds to 2 decimal places. The argument from the user input is passed through both functions.
