# Local Variable

**Description:** A local variable is created inside a function or procedure and only exists while that subroutine is running - it cannot be accessed from outside it. This stops different parts of a program interfering.

## Example
```python
def calculateArea():
    length = 5   # local variable
    width = 3     # local variable
    return length * width

print(calculateArea())
# length and width don't exist out here
```

# Local Variable — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure creates a local variable called message, stores "Hello, world!" in it and prints it. There are 3 errors — order, the local variable not declared inside the function and indentation.
**Hint:** A local variable is declared inside the function — it belongs to that function only. The function must be defined before it is called. Fix the indentation of both lines inside the function.

```python
greet()
def greet():
message = "Hello, world!"
print(message)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the function creates a local variable score = 100 and prints "Inside: 100". Then explain why the second print outside the function would crash. There are 3 errors — missing colon, wrong value and indentation.
**Hint:** A local variable only exists inside the function where it is created. Check the def line for a missing colon. The value should be 100 not "100" (no quotes). Fix the indentation of both lines inside the function.

```python
def setScore()
    score = "100"
print("Inside:", score)
setScore()
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the procedure so it uses a local variable called status to store "hot", "warm" or "cold" depending on the temperature, then prints it. checkTemp(35) should print "It is hot". There are 4 errors — missing colon, local variable not initialised, wrong comparison and indentation.
**Hint:** Declare status = "" at the start of the function. Check the def line for a missing colon. 30 degrees should be hot — check which comparison operator is used. Fix the indentation of the print.

```python
def checkTemp(temp)
    if temp > 30:
        status = "hot"
    elif temp > 15:
        status = "warm"
    else:
        status = "cold"
print("It is", status)
checkTemp(35)
checkTemp(20)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the procedure so it uses a local variable count and a for loop to count down from start to 1 then prints "Done!". countDown(5) should print 5, 4, 3, 2, 1 then "Done!". There are 4 errors — missing colon, local variable used before declared, wrong range and indentation.
**Hint:** Declare count = start inside the function before the loop. Check the def line for a missing colon. range(start, 0, -1) counts down to 1. Fix the indentation of the print inside the loop and the "Done!" after it.

```python
def countDown(start)
    for i in range(start):
        print(count)
    count = start
print("Done!")
countDown(5)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the procedure so it uses a local variable total to accumulate the sum of a list and prints "Sum: 100". Passing [10, 20, 30, 40] should print Sum: 100. There are 4 errors — missing colon, local variable not initialised to 0, wrong operator and indentation.
**Hint:** total must start at 0 before the loop. Check the def line for a missing colon. Adding to a running total uses + not *. The print must be outside (after) the loop but still inside the function.

```python
def sumList(numbers)
    total = 10
    for n in numbers:
        total = total * n
        print("Sum:", total)
sumList([10, 20, 30, 40])
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the procedure so it uses a local counter variable in a while loop to print numbers from 0 up to (but not including) limit. countUp(4) should print 0, 1, 2, 3. There are 4 errors — missing colon, counter starts at wrong value, wrong loop condition and counter not incremented.
**Hint:** The counter should start at 0. The while condition should check counter < limit. Add counter += 1 inside the loop or it will run forever. Fix the def line.

```python
def countUp(limit)
    counter = 1
    while counter > limit:
        print(counter)
countUp(4)
```

## Challenge 7
**Type:** write
**Difficulty:** medium
**Task:** Write two separate procedures — functionA and functionB. Each should declare a local variable called result with a different string value and print it. Call both. This shows that two functions can use the same local variable name without conflict.
**Hint:** Local variables belong to their own function — result in functionA and result in functionB are completely separate. Define both, then call both.

## Challenge 8
**Type:** debug
**Difficulty:** medium
**Task:** Fix the procedure so it creates a local list called names, appends three names to it and prints each one on a separate line using a for loop. There are 4 errors — missing colon, list not initialised as empty, wrong method name and indentation.
**Hint:** Declare names = [] inside the function. Check the def line for a missing colon. The method to add to a list is append() — check the spelling. Fix the indentation of the for loop and print.

```python
def buildList()
    names = ""
    names.apend("Raj")
    names.append("Sam")
    names.append("Amy")
    for name in names:
    print(name)
buildList()
```

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Write a function called highestScore that takes a list of scores as a parameter. Use a local variable called highest, set it to the first item in the list, then use a for loop and if statement to find the largest value. Return highest. Test with scores = [55, 88, 72, 91, 63] — it should print "Highest: 91".
**Hint:** Set highest = scores[0] as your starting point. Loop through the list — if any score is greater than highest, update highest. Return highest after the loop. The variable highest is local to the function.

```python
scores = [55, 88, 72, 91, 63]
```

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Declare a variable name = "Global Alex" outside any function. Write a procedure called showName that declares its own local variable also called name = "Local Sam" and prints it. Call the procedure, then print name outside the function. The output should show that the local variable inside the function does not affect the one outside.
**Hint:** The local variable inside showName is completely separate from the one outside. After calling showName(), print name — it should still be "Global Alex". This is what makes local variables safe to use.
