# Passing — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so "Priya" is passed to the procedure and it prints "Name: Priya". There are 3 errors — order, wrong value passed and indentation.
**Hint:** The procedure must be defined before the call. Check what string is being passed — it should be "Priya" not "name". The print must be indented inside the procedure.

```python
printName("name")
def printName(name):
print("Name:", name)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the integer 78 is passed and prints "Your score is 78 out of 100". There are 3 errors — the value passed is a string not an integer, missing colon and indentation.
**Hint:** Passing "78" (with quotes) gives a string. Passing 78 (no quotes) gives an integer. Check the def line for a missing colon. Fix the indentation of the print.

```python
def showScore(score)
print("Your score is", score, "out of 100")
showScore("78")
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so two strings are passed and it prints "Ada Lovelace". There are 3 errors — wrong number of arguments passed, missing space in the join and indentation.
**Hint:** The procedure has two parameters — the call must pass two arguments. Check the return/print statement — is there a space between first and last? Fix the indentation.

```python
def fullName(first, last):
print(first + last)
fullName("Ada")
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so a variable is passed to the procedure and it prints 15. There are 4 errors — missing colon, wrong operator, variable declared after the call and the variable not passed in the call.
**Hint:** The procedure must be defined and the variable declared before the call. Triple means multiply by 3 not add 3. Pass the variable name inside the brackets of the call.

```python
def triple(n)
    print(n + 3)
triple()
userNum = int(input("Enter a number: "))
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the result of input() is passed directly to the procedure which prints it in uppercase. Typing "hello" should print "HELLO". There are 3 errors — missing colon, wrong method name and the input not being passed in the call.
**Hint:** Check the def line for a missing colon. The method to convert to uppercase is .upper() not .uppercase(). Pass input() directly inside the brackets of the call.

```python
def shout(word)
    print(word.uppercase())
shout()
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so a temperature in Fahrenheit is passed to toCelsius, converted and then passed to showCelsius for display. Passing 212 should print "Celsius: 100.0". There are 4 errors — missing colons, wrong formula and the converted value not passed to showCelsius.
**Hint:** The conversion formula is (temp - 32) * 5/9 not (temp + 32) * 5/9. Check both def lines for missing colons. The result of toCelsius(f) should be passed as the argument to showCelsius.

```python
def showCelsius(temp)
    print("Celsius:", temp)
def toCelsius(temp)
    return round((temp + 32) * 5/9, 1)
f = int(input("Enter Fahrenheit: "))
showCelsius(f)
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so each item from the list is passed to the procedure on each loop. It should print "The animal is a cat", "The animal is a dog", "The animal is a rabbit". There are 3 errors — missing colon, wrong variable passed in the call and indentation.
**Hint:** The loop variable is called pet — that is what should be passed to the procedure each time. Check the def line for a missing colon. The call must be indented inside the for loop.

```python
def describe(animal)
    print("The animal is a", animal)
pets = ["cat", "dog", "rabbit"]
for pet in pets:
describe(pets)
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Write a procedure called checkPass that takes one parameter called passed (a bool). If passed is True print "Well done, you passed!", otherwise print "Better luck next time". Call it twice — once passing True and once passing False.
**Hint:** Pass the boolean values True and False directly as arguments — no quotes needed. Use if passed: as the condition inside the procedure.

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Write a procedure called isEven that takes one parameter n. Inside, use % to check if n is even or odd and print the appropriate message e.g. "2 is even" or "3 is odd". Use a for loop with range(1, 6) to pass the numbers 1 to 5 to the procedure.
**Hint:** n % 2 == 0 means n is even. Pass the loop variable directly to isEven inside the loop. The procedure is called once per iteration with a different argument each time.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Write three functions: getScore() that returns an integer entered by the user, getGrade(score) that returns "Distinction" for 70+, "Merit" for 50+ or "Pass" otherwise, and showResult(score, grade) that prints both. Call getScore(), store the result, then pass it to both getGrade() and showResult(). For a score of 85, output should be "Score: 85 | Grade: Distinction".
**Hint:** Store the return value of getScore() in a variable. Pass that variable to getGrade() and store that result too. Then pass both to showResult() as two separate arguments.
