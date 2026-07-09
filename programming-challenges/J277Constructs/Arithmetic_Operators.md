# Arithmetic Operators

**Description:** Arithmetic operators perform maths on numeric values: + - * / for the basics, // for integer division, % for remainder (modulus), and ** for powers. They are used constantly for totals, averages and scores.

## Example 1
```python
a = 17
b = 5
print(a + b, a - b, a * b)
print(a // b)   # integer division -> 3
print(a % b)    # remainder -> 2
```

## Example 2
```python
base = 2
power = 8
print(base ** power)   # 2 to the power of 8
```

## Example 3
```python
print(2 + 3 * 4)          # BODMAS: * before + -> 14
print((2 + 3) * 4)        # brackets change the order -> 20
```
# Arithmetic Operators — Challenges

## Challenge 1
**Type:** write
**Difficulty:** easy
**Task:** Run the code. It uses the four basic arithmetic operators. Write a comment next to each print() explaining what operator it uses and what the output will be before you run it.
**Hint:** The four operators are + - * /. Note that dividing two integers in Python 3 always returns a float.

```python
print(10 + 5)
print(10 - 5)
print(10 * 5)
print(10 / 5)
```

## Challenge 2
**Type:** write
**Difficulty:** easy
**Task:** Run the code and study the three outputs. Write a comment next to each line explaining the difference between /, // and %. Then write three more examples of your own using different numbers.
**Hint:** / gives a float result. // gives the whole number part only (floor division). % gives the remainder after division.

```python
print(10 / 3)
print(10 // 3)
print(10 % 3)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** The code calculates a quiz score. A student got 5 questions right, each worth 10 points, plus a 50 point bonus. The answer should be 100. Fix the 2 operator errors.
**Hint:** Think carefully about each operator — adding questions to points per question is not the same as multiplying them. And a bonus should increase the total, not decrease it.

```python
score = 5
pointsPerQuestion = 10
bonus = 50
total = score + pointsPerQuestion
totalWithBonus = total - bonus
print("Score:", totalWithBonus)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** The code below is meant to show that BODMAS (order of operations) matters. The first print should give 14, the second should give 20. Fix the error on line 2.
**Hint:** Python follows BODMAS — multiplication happens before addition. To change the order, use brackets.

```python
print(2 + 3 * 4)
print(2 + 3 * 4)
```

## Challenge 5
**Type:** write
**Difficulty:** medium
**Task:** Use the modulo operator (%) to write a program that loops through the numbers 1 to 20 and displays whether each number is even or odd.
**Hint:** Any number % 2 gives either 0 (even) or 1 (odd). Use an if/else inside a for loop.

## Challenge 6
**Type:** write
**Difficulty:** medium
**Task:** A film is 137 minutes long. Write a program that uses // and % to display the length in hours and minutes. Expected output: "2 hours and 17 minutes".
**Hint:** Use // to get the whole number of hours. Use % to get the remaining minutes.

```python
minutes = 137
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** The ** operator raises a number to a power. Write a program that displays: 2 to the power of 8, 3 cubed, and 5 squared. Run it and check your answers.
**Hint:** 2 ** 8 means 2 multiplied by itself 8 times. The answer is 256.

## Challenge 8
**Type:** write
**Difficulty:** hard
**Task:** A shop sells items at £3.99 each. A customer buys 4. They get a 10% discount. Write a program that calculates and displays the total after discount. Expected output: "Total: £ 14.36"
**Hint:** Calculate subtotal first (price * quantity). Then subtract 10% of the subtotal. Use round(value, 2) to display 2 decimal places.

## Challenge 9
**Type:** debug
**Difficulty:** hard
**Task:** The code uses the power operator and modulo operator but with the wrong symbols. Fix the 2 errors so the code displays 256 and 2.
**Hint:** In Python, the power operator is two asterisks (**), not the caret symbol (^). The modulo operator is %, not the word "mod".

```python
print(2 ^ 8)
print(17 mod 5)
```

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Write a compound interest calculator. Start with £1000, an interest rate of 5% per year, and calculate the total after 3 years. Expected output: "£ 1157.63". Use the formula: amount = principal * (1 + rate) ** years.
**Hint:** You will need the ** operator for the power. Use round(amount, 2) to get 2 decimal places.

```python
principal = 1000
rate = 0.05
years = 3
```
