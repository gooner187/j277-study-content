# String Slicing

**Description:** String slicing extracts part of a string using index positions in the form string[start:end], where the end index is not included. It is useful for tasks like getting initials or a file extension.

## Example
```python
word = "Computing"
print(word[0:4])   # "Comp" - indices 0 to 3
print(word[-3:])    # "ing" - last 3 characters
print(word[0])       # "C" - single character
```

# String Slicing — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** The code is meant to display just "Ali" from "Muhammad Ali". Test it, see what it actually prints, then fix the 1 error.
**Hint:** Count the index positions carefully — Python starts counting from 0. What index does "A" in "Ali" sit at?

```python
boxer = "Muhammad Ali"
surname = boxer[7:11]
print(surname)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** The code uses negative indexing to display "Ali" but it prints " Ali" with a space at the front. Fix the 1 error.
**Hint:** Negative indexing counts from the end of the string. boxer[-1] is "i", boxer[-2] is "l", boxer[-3] is "A". How many characters is "Ali"?

```python
boxer = "Muhammad Ali"
surname = boxer[-5:]
print(surname)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** The code is meant to display the number of characters in the boxer's name including the space (answer: 12). Fix all the errors.
**Hint:** There are 3 errors — look carefully at the variable names for a zero used instead of a letter, a capital letter where there should not be one, and a spelling mistake.

```python
boxer = "muhammad Ali"
length = len(b0xer)
prInt(lemgth)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** The code is meant to display "Muhammad" on one line and "Ali" on the next. Fix all the errors — there are 4.
**Hint:** Check the slice indices for both firstName and surname — count from index 0. Also look carefully at the variable names used in both print statements.

```python
boxer = "Muhammad Ali"
firstName = boxer[4:8]
surname = boxer[9:11]
print(f1rstName)
print(surnane)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** The code is meant to display "Muhammad THE GOAT Ali". Test it, see what it prints, then fix the 3 errors.
**Hint:** Check both slice indices. Also check the last argument in the final print — it should display the surname, not the first name again.

```python
boxer = "Muhammad Ali"
status = " THE GOAT "
firstName = boxer[3:8]
surname = boxer[9:11]
print(firstName + status + firstName)
```

## Challenge 6
**Type:** debug
**Difficulty:** easy
**Task:** The code asks the user for their first name and should tell them the first letter. It is not working. Fix the 2 errors.
**Hint:** String indexing starts at 0, not 1 or 2. Also check the spelling of the print function.

```python
name = str(input("Enter your first name>>>"))
letter = name[2]
primt("Your name begins with", letter)
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** The code asks for a name and should display the first and last letter. It is not working. Fix the 3 errors.
**Hint:** Look for a typo in the input function name. Check which variable is used in the first print statement — it says "begins with" but is it using the right variable? Also check the second print function spelling.

```python
name = str(imput("Enter your fidrst name>>>"))
firstLetter = name[0]
lastLetter = name[-1:]
print("Your name begins with", lastLetter)
pr1nt("Your name ends with", lastLetter)
```

## Challenge 8
**Type:** debug
**Difficulty:** medium
**Task:** The code is meant to slice out "THE CHAMP" from the string and display only that. Fix the 2 errors.
**Hint:** Count the character positions carefully — where does "THE CHAMP" start and end? Also check what is being passed to the final print statement.

```python
boxer = "Muhammad THE CHAMP Ali"
nickname = boxer[9:23]
print(boxer)
```

## Challenge 9
**Type:** debug
**Difficulty:** hard
**Task:** The code converts a UK mobile number starting with 0 to international format by replacing the 0 with +44. For example 07956111222 becomes +447956111222. It is not working correctly. Fix the 1 error.
**Hint:** Look at the line that builds the international number — how many times is the prefix being added?

```python
ukNumber = input("enter UK number>>>")
preFix = "+44"
if ukNumber[0] == "0":
    ukNumber = ukNumber[1:]
    ukNumber = preFix + preFix + ukNumber
    print("International: ", ukNumber)
else:
    print("Not recognised")
```

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Write a program that asks the user to enter their first name, last name and a nickname. Display the number of characters in the first name, then the number of characters in the last name. Then display the full name with the nickname in the middle — e.g. "Ada THE LEGEND Lovelace".
**Hint:** Use len() to count characters. Use string concatenation to build the final display with spaces around the nickname.
