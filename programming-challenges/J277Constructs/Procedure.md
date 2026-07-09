# Procedure

**Description:** A procedure is a named, reusable block of code that performs a task but does not send a value back to where it was called. In J277 it is written with def like a function, but has no return statement.

## Example
```python
def greetUser(name):   # a procedure - no return
    print("Hello,", name)
    print("Welcome!")

greetUser("Priya")       # calling the procedure
```

# Procedure — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the three lines of code so the procedure is defined and called correctly. It should display "Happy new year!". Check the order and indentation.
**Hint:** In Python, a procedure (def) must be defined before it is called. The print statement must be indented inside the def block.

```python
newYear()
def newYear():
print("Happy new year!")
```

## Challenge 2
**Type:** debug
**Difficulty:** medium
**Task:** Fix all the errors so the procedure asks for two numbers, adds them and displays the total. There are 5 errors — syntax, typos and indentation.
**Hint:** Check the parameter names in the def line — are they both the same? Look for a missing colon. Check the spelling of input(). Check the variable name used in the call. Fix the indentation inside the procedure.

```python
def adding(num1, num1)
total=num1 + num2
print(total)
number1=int(input("Enter a number: "))
number2=int(inplop("Enter another number: "))
adding(number1, numberd2)
```

## Challenge 3
**Type:** debug
**Difficulty:** medium
**Task:** Fix all the errors so the procedure asks for two numbers, multiplies them and displays the answer. There are 4 errors — order, variable name mismatch, wrong data type and a missing procedure call.
**Hint:** print(total) cannot come before total is calculated. Check the parameter name used inside the procedure — does it match what was declared? Should the second input be a str or an int? Don't forget to call the procedure at the end.

```python
def multiply(num1, numTwo):
print(total)
total = num1*num2
numbre1=int(input("Enter a number: "))
number2=str(input("Enter another number: "))
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix all the errors so the procedure sings happy birthday using a name entered by the user. There are 5 errors — order, wrong data type, wrong variable names and indentation.
**Hint:** The procedure must be defined before it is called. Check the data type used for the name input — should it be int or str? Check the parameter name in the def line versus what is used inside. Check what variable name is passed in the call.

```python
def happyBirthday(names):
print("Happy birthday to you")
    print("Happy birthday to you")
print("Happy birthday dear", name)
        print("Happy birthday to you")
happyBirthday(named)
name=int(input("Enter birthday name:>>>"))
```

## Challenge 5
**Type:** debug
**Difficulty:** hard
**Task:** Fix all the errors in the menu procedure. It should display a menu, ask for a choice and display the correct response. There are 6 errors — a missing colon, wrong data type, two logic errors, indentation and order.
**Hint:** Add the missing colon after def menu(). Should choice be a float or int? Check the first if condition — does choice >= 1 work correctly for a menu? Check the last elif — != is not the same as ==. Fix all indentation so everything is inside the procedure.

```python
def menu()
    else:
        print("Invalid choice")
        
print("Welcome to the game")
print("press 1 for 1-player")
    print("press 2 for 2-player")
    print("press 3 for online")
    menu()
       choice = float(input("Enter 1, 2 or 3:>>>"))
     if choice >= 1:
   print("1-player chosen")
    elif choice == 2:
        print("2-player chosen")
    elif choice != 3:
        print("online chosen")
```

## Challenge 6
**Type:** extend
**Difficulty:** medium
**Task:** The code below works — test it. Add a third procedure called getFavFood() that asks the user for their favourite food and returns it. Update start() to also print "your favourite food is:" followed by the result.
**Hint:** Follow the same pattern as getName() and getAge(). Use input() to get the food, return it, and call it inside start() with a print statement.

```python
def getName():
  name = str(input("Enter first name >>>"))
  return name
def getAge():
  age = int(input("Enter your age >>>"))
  return age
def start():
  print("you name is:",getName())
  print("you age is:",getAge())
  
start()
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** Create a procedure called circleArea that has one parameter called radius. Inside, calculate the area using the formula PI x radius x radius and print the result rounded to 2 decimal places. Ask the user to enter a radius, then call the procedure with it.
**Hint:** Declare PI = 3.141592653 before the procedure. Use round(area, 2) to round to 2 decimal places. Call the procedure after getting the user's input.

```python
PI = 3.141592653
```
