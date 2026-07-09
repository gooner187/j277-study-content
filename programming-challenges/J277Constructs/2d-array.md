# 2D Array

**Description:** A 2D array is a list of lists, used to store data in a grid of rows and columns, such as a seating plan or a game board. Each item is accessed using two indices - one for the row, one for the column.

## Example
```python
grid = [[1, 2, 3], [4, 5, 6]]   # 2 rows, 3 columns
print(grid[0][1])                # row 0, column 1 -> 2
grid[1][2] = 99                   # update row 1, column 2
print(grid)
```

# 2D Array — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** The code below has syntax errors. Fix them so the menu array prints correctly. There are 4 errors to find.
**Hint:** Look carefully at missing commas, brackets, and spelling of the function and variable names.

```python
menu =  [
        [1, "Kebab", "salad", "drink"],
[2, "Burger", "chips", "drink"]
        [3, "Pizza", "Garlic bread" "drink"],
        ]
primt(memu)
```

## Challenge 2
**Type:** debug
**Difficulty:** medium
**Task:** The code below is meant to display a menu, ask the user to choose a meal and then display their choice. Fix all syntax, logical and indentation errors. There are 8 errors.
**Hint:** Check the data type of `choice` compared to what it is being compared to. Check array indices are integers. Look for missing colons, wrong brackets and indentation.

```python
menu =  [
        [1, "Kebab", "salad", "drink"],
        [2, "Burger", "chips", "drink",
        [3, "Pizza", "Garlic bread", "drink"]
        ]
print(temu)
choice = str(input("Choose a meal - 1, 2 or 3: "))
if choice == 1
array1 = 0
    print(menu[array1])
        elif choice == 2:
    array2 = 1.3
    print(menu[array2])
else:
    array3 = 2
    print(menu(array3])
```

## Challenge 3
**Type:** write
**Difficulty:** easy
**Task:** Create a 2D array that holds these facts about 3 planets and then displays the full array. Each row should contain: number, planet name, type, position from Sun.
**Hint:** Each row in the 2D array is itself a list. Your outer list holds all three rows.

```python
# 1, Jupiter, Gas giant, 5th from Sun
# 2, Saturn, Gas giant, 6th from Sun
# 3, Uranus, Ice giant, 7th from Sun
```

## Challenge 4
**Type:** debug
**Difficulty:** easy
**Task:** The code below is meant to declare an empty array and then place two arrays into it to make a 2D array. Fix all the errors.
**Hint:** Check brackets match, check the assignment operator, check spelling of method names, and check which array is being appended the second time.

```python
emptyArray = []
print(emptyArray)
planets = ["Earth", "Saturn", "Mars")
colours == ["red", "green", "blue"]
emptyArray.append(planets)
print(emptyArray)
emptyArray.appond(planets)
print(emptyAray)
```

## Challenge 5
**Type:** debug
**Difficulty:** easy
**Task:** The code below is meant to display the 2D array like a table, one row per line. Fix the for loop.
**Hint:** The loop variable holds each row — that is what should be printed, not the whole array.

```python
planets =   [
            [1, "Jupiter", "Gas giant", "5th from Sun"],
            [2, "Saturn", "Gas giant", "6th from Sun"],
            [3, "Uranus", "Ice giant", "7th from Sun"],
            ]
for variableToHoldArray in planets:
    print(planets)
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** The code below is meant to display the year 2003 and the number of trophies Tottenham won that year. There are logic errors only — fix the array indices.
**Hint:** Count the rows carefully. Row 0 is the header. Which row is 2003? Which column holds trophies?

```python
Tottenham = [
            ["Year","Trophies"],
            [2002, 0],
            [2003, 0],
            [2004, 0],
            ]
print("in the year", Tottenham[1][1])
print("Tottenham won", Tottenham[3][0], "trophies")
```

## Challenge 7
**Type:** extend
**Difficulty:** medium
**Task:** Tottenham won 0 trophies in the next three years. The code below has been started — finish it. Use a for loop to display all years and trophies won in the same format as Challenge 6.
**Hint:** Use `range(1, len(Tottenham))` to skip the header row. Access year with `[i][0]` and trophies with `[i][1]`.

```python
Tottenham = [
            ["Year","Trophies"],
            [2002, 0],
            [2003, 0],
            [2004, 0],
            [2005, 0],
            [2006, 0],
            [2007, 0],
            ]
for i in range(len(Tottenham)-1):
    pr
```

## Challenge 8
**Type:** debug
**Difficulty:** hard
**Task:** The code below is meant to add up all the trophies won by Arsenal and display the total (which should be 5). Fix all the errors.
**Hint:** There are 4 errors — check the starting value of totalTrophies, the range, the array indices, and the spelling of the variable in the print statement.

```python
Arsenal =  [
            ["Year","Trophies"],
            [2002, 2],
            [2003, 1],
            [2004, 2],
            ]
totalTrophies = 13
for counter in range(1):
    totalTrophies = totalTrophies + Arsenal[counter+4][0]
print("Total trophies won: ", totolTrophies)
```

## Challenge 9
**Type:** extend
**Difficulty:** hard
**Task:** Upgrade the Arsenal code from Challenge 8. Display the full 2D array as a table (year and trophies on each row), then display the total trophies won at the end.
**Hint:** Use a for loop to print each row, skipping the header. Then use a second loop (or the same one) to accumulate the total.

```python
Arsenal =  [
            ["Year","Trophies"],
            [2002, 2],
            [2003, 1],
            [2004, 2],
            ]
```
