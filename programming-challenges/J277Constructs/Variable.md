# Variable

**Description:** A variable is a named location in memory that stores a value which can change while the program runs. Every algorithm in J277 relies on variables to store, update and reuse data as a program executes.

## Example 1
```python
name = "Ada"          # store some text
age = 16              # store a number
age = age + 1         # update the value
print(name, "is", age)
```

## Example 2
```python
temperature = 18          # store today's temperature
print("It is", temperature, "degrees")
temperature = 21          # the variable's value changes
print("Now it is", temperature, "degrees")
```

## Example 3
```python
score = 0                 # a variable used as a running total
score = score + 10        # variables can be updated using their own value
score = score + 5
print("Final score:", score)
```
# Variable — Challenges

## Challenge 1
**Type:** write
**Difficulty:** easy
**Task:** Create a variable called "name" and store your first name in it. Then print it. Simple as that!
**Hint:** A variable stores a value. Use = to assign it. Text values need speech marks around them.

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** The code should print the number 16 but there is a typo in the variable name inside print(). Fix the 1 error.
**Hint:** The variable is declared as "age" — check the spelling inside print() carefully.

```python
age = 16
print(aeg)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** The code should print 10 but prints 0 instead. Fix the 1 error — the variable is not being updated correctly.
**Hint:** To increase a variable by 10 you need to use the variable itself on the right hand side of =. score = 10 replaces the value. score = score + 10 adds to it.

```python
score = 0
score = 10
print(score)
```

## Challenge 4
**Type:** write
**Difficulty:** easy
**Task:** Two variables a = 5 and b = 10 need to swap their values so that a becomes 10 and b becomes 5. Write the code to swap them and print both. Expected output: "10 5".
**Hint:** You need a third temporary variable to hold one value while you swap. Try: temp = a, then a = b, then b = temp.

```python
a = 5
b = 10
```

## Challenge 5
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "Raj has 3 lives" but crashes with a TypeError. Fix the 1 error.
**Hint:** You cannot join a string and an integer with +. Convert lives to a string first using str().

```python
playerName = "Raj"
lives = 3
print(playerName + " has " + lives + " lives")
```

## Challenge 6
**Type:** write
**Difficulty:** easy
**Task:** Write a program that asks the user to enter their name using input(), stores it in a variable called "name", then prints "Hello" followed by the name.
**Hint:** Use name = input("What is your name? ") to store what the user types. Then use print() with both words.

## Challenge 7
**Type:** write
**Difficulty:** easy
**Task:** Create two variables: length = 8 and width = 5. Create a third variable called "area" that calculates length multiplied by width. Print "Area: 40".
**Hint:** Use the * operator to multiply. Store the result in a new variable before printing it.

## Challenge 8
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "Sam Jones" but uses the wrong variable names inside print(). Fix the 2 errors.
**Hint:** Check the exact names of the variables declared at the top — Python is case sensitive and the names must match exactly.

```python
firstName = "Sam"
lastName = "Jones"
print(first + " " + last)
```

## Challenge 9
**Type:** extend
**Difficulty:** easy
**Task:** The code sets a price and prints it. Extend it to increase the price by 2 and print the new price. Expected output: "Original price: £ 5" then "New price: £ 7".
**Hint:** Use price = price + 2 to update the variable. Then print it again.

```python
price = 5
print("Original price: £", price)
```

## Challenge 10
**Type:** write
**Difficulty:** easy
**Task:** Create a variable called "temperature" and set it to 22. Write an if/else statement that prints "It is warm" if temperature is above 20, otherwise prints "It is cold".
**Hint:** Use if temperature > 20: for the condition. The else: branch handles everything else.
