# Constant — Challenges

## Challenge 1
**Type:** write
**Difficulty:** easy
**Task:** In Python, constants are written in UPPER_CASE to show they should not change. Create a constant called PI = 3.14159 and a variable radius = 5. Calculate the area of a circle (PI * radius * radius) and print the result. Expected output: 78.53975.
**Hint:** Use UPPER_CASE for the constant name. area = PI * radius * radius calculates the area. Then print it.

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Constants should be written in UPPER_CASE by convention. Fix the code so the constant follows the correct naming convention and still prints 100.
**Hint:** Rename the constant from lowercase to uppercase. Remember to update both the declaration and the print statement.

```python
max_score = 100
print(max_score)
```

## Challenge 3
**Type:** write
**Difficulty:** easy
**Task:** Create a constant SPEED_LIMIT = 30 and a variable speed = 25. Write an if/else statement that prints "Too fast!" if speed is above the speed limit, otherwise prints "Safe speed".
**Hint:** Use the constant name in your if condition — if speed > SPEED_LIMIT: — this is the whole point of a constant, so the limit is easy to find and change later.

## Challenge 4
**Type:** write
**Difficulty:** easy
**Task:** Create a constant VAT = 0.20 and a variable price = 50. Calculate the total price including VAT and print "Total: £ 60.0".
**Hint:** Total = price + (price * VAT). The constant makes it easy to change the VAT rate in one place if it ever changes.

## Challenge 5
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "Fail" because studentScore is 45 and PASS_MARK is 50. There is 1 error — someone has tried to change the constant. Fix it.
**Hint:** A constant should never be reassigned after it is declared. Remove the line that tries to change PASS_MARK.

```python
PASS_MARK = 50
studentScore = 45
PASS_MARK = 40
if studentScore >= PASS_MARK:
    print("Pass")
else:
    print("Fail")
```

## Challenge 6
**Type:** write
**Difficulty:** easy
**Task:** Create two constants: HEADS = 1 and TAILS = 0. Create a variable flip = 1. Write an if/else that prints "Heads!" if flip equals HEADS, otherwise prints "Tails!".
**Hint:** Compare flip to the constant using ==. Using named constants makes the code much easier to read than comparing to 0 and 1 directly.

## Challenge 7
**Type:** write
**Difficulty:** easy
**Task:** Create a constant POINTS_PER_GOAL = 3 and a variable goals = 4. Calculate the total points and print "Points: 12".
**Hint:** Multiply goals by the constant. If the points value ever changes you only need to update the constant in one place.

## Challenge 8
**Type:** debug
**Difficulty:** medium
**Task:** The code should calculate weight using the formula mass * GRAVITY. Fix the 2 errors — the constant name is wrong and the variable name is wrong in the calculation.
**Hint:** Check the spelling of the constant and the variable name used in the weight calculation — they must match exactly what was declared.

```python
GRAVITY = 9.8
mass = 70
weight = Mass * gravity
print("Weight:", weight, "N")
```

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Create a constant MIN_AGE = 18. Ask the user to enter their age using input() and store it in a variable. Write an if/else that prints "Access granted" if age is 18 or over, otherwise prints "Too young".
**Hint:** input() returns a string so you need int() to convert it before comparing to MIN_AGE.

## Challenge 10
**Type:** write
**Difficulty:** medium
**Task:** Create a constant DISCOUNT = 0.15 and a variable originalPrice = 80. Calculate the sale price after the discount is applied and print "Sale price: £ 68.0".
**Hint:** salePrice = originalPrice - (originalPrice * DISCOUNT). The constant means if the discount rate changes you only update one line.
