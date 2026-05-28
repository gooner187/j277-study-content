# List / 1D Array — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the syntax error so the code prints all items in the array. There is 1 error.
**Hint:** Look carefully at the variable name inside print().

```python
bag = ["keys", "Money", "Pen"]
print(hag)
```

## Challenge 2
**Type:** write
**Difficulty:** easy
**Task:** Create an array called "Oceans" containing the 5 world oceans. Write code to display the full array.
**Hint:** The 5 oceans are: Pacific, Atlantic, Indian, Southern, Arctic.

## Challenge 3
**Type:** debug
**Difficulty:** medium
**Task:** Fix the syntax and logic errors. The code should display the bag contents, then ask the user to enter 1, 2 or 3 and display that item. There are 2 errors.
**Hint:** Check the spelling of the variable used as the index. Also check the data type of choice — can a string be used as an array index?

```python
bag = ["keys", "Money", "Pen"]
print(bag)
choice = str(input("Enter 1, 2 or 3"))
bagItem = bag[choize-1]
print(bagItem)
```

## Challenge 4
**Type:** debug
**Difficulty:** easy
**Task:** Fix all syntax errors and indentation so the code displays each item on a new line. There are 4 errors.
**Hint:** Check the for loop indentation, the array name, the variable name inside print, and where print sits relative to the loop.

```python
bag = ["keys", "Money", "Pen"]
   for item in bagg:
print(kebab)
```

## Challenge 5
**Type:** debug
**Difficulty:** easy
**Task:** Fix all syntax errors. The code should ask for 3 names, add them to an array and then display the array. There are 2 errors.
**Hint:** Check the variable name used with append() on line 3. Check the spelling of the method name on line 4.

```python
names = []
names.append(input("Enter name1 >>>"))
name.append(input("Enter name2 >>>"))
names.appnd(input("Enter name3 >>>"))
print(names)
```

## Challenge 6
**Type:** write
**Difficulty:** medium
**Task:** Write a program that declares an empty array, asks the user to enter 3 names and adds each one to the array using append(), then displays each name on a separate line using a loop.
**Hint:** Start with an empty array [], use append() three times, then use a for loop to print each item.

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** The code should display names beginning with "R". Fix all syntax errors and indentation. There are 4 errors.
**Hint:** Check the for loop indentation and missing colon. Check the comparison operator inside the if statement. Check the print statement carefully.

```python
people = ["Raj", "Rik", "Saha"]
    for name in people
if name[0] = "R":
print(name
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Create an array with 5 different animals. Loop through the array to display each one like this: "Number 1 animal is a cat", "Number 2 animal is a dog" and so on.
**Hint:** You need a counter that increases with each loop.

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Using the array testMarks = [66, 78, 45, 88, 73] and a pass mark of 75, write code that displays the array, then counts and displays how many students passed and how many failed.
**Hint:** Use two counter variables starting at 0. Loop through the array and use an if/else to increment the correct counter each time.

```python
testMarks = [66, 78, 45, 88, 73]
```

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Create an empty array called "colours". In a loop, ask the user to press x to exit or enter a colour. Each colour should be added to the array. When x is pressed, display the full array and the number of colours entered.
**Hint:** Use a while loop with a condition that checks for "x". Use append() to add each colour. Use len() to count the colours at the end.
