# Concatenation — Challenges

## Challenge 1
**Type:** write
**Difficulty:** easy
**Task:** Create two variables: firstName = "Ada" and lastName = "Lovelace". Join them together with a space in between and print the full name. Expected output: "Ada Lovelace".
**Hint:** Use + to join strings. Don't forget to add a space between the two names — " " is a string containing a space.

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "New York" but prints "NewYork" instead. Fix the 1 error.
**Hint:** When you join two strings with + there is no automatic space. You need to add " " between them.

```python
city = "New"
country = "York"
print(city + country)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** The code should print "I am 14 years old" but crashes with a TypeError. Fix the 1 error.
**Hint:** You cannot join a string and an integer with +. Convert age to a string first using str().

```python
age = 14
print("I am " + age + " years old")
```

## Challenge 4
**Type:** write
**Difficulty:** easy
**Task:** Ask the user to enter their first name and then their last name using two separate input() statements. Join them together with a space and print "Full name: Ada Lovelace" (using whatever the user typed).
**Hint:** Store each input in a separate variable. Then join them: "Full name: " + firstName + " " + lastName.

## Challenge 5
**Type:** write
**Difficulty:** easy
**Task:** Create variables: item = "pencils", quantity = 5, price = 2. Calculate the total cost and print: "You bought 5 pencils for £10". All values must come from the variables.
**Hint:** Calculate total = quantity * price first. Use str() to convert numbers before joining them with +.

## Challenge 6
**Type:** write
**Difficulty:** medium
**Task:** Create a list: words = ["Python", "is", "fun"]. Use a for loop to build a single string by joining all the words together with spaces. Print the result: "Python is fun".
**Hint:** Start with an empty string sentence = "". In the loop, add each word plus a space: sentence = sentence + word + " ". After the loop, print sentence.

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** The code should build a string of names separated by commas but the loop uses the wrong variable. Fix the 1 error.
**Hint:** The loop variable is called "name" — check what variable is being added inside the loop.

```python
names = ["Raj", "Sam", "Amy"]
result = ""
for name in names:
    result = result + person + ", "
print(result)
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Create a list: scores = [45, 72, 88, 31, 65]. Use a for loop and an if statement to build a string of only the scores that are 50 or above. Print "Passed: 72 88 65".
**Hint:** Start with passed = "Passed: ". In the loop, check if score >= 50. If so, add str(score) + " " to passed. Print after the loop.

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Use a for loop that runs 3 times. Each time, ask the user to enter a word using input() and show which number word it is e.g. "Enter word 1: ". Build all three words into one sentence and print it.
**Hint:** Use range(3) for the loop. The loop variable i starts at 0 so use str(i+1) for the word number. Build the sentence by adding each word + " " each time.

## Challenge 10
**Type:** debug
**Difficulty:** medium
**Task:** The code should print "Animals: cat dog bird" but uses the wrong variable inside the loop. Fix the 1 error.
**Hint:** Check what the for loop variable is called — the variable being joined inside the loop must match the loop variable name exactly.

```python
animals = ["cat", "dog", "bird"]
result = "Animals: "
for animal in animals:
    result = result + pet + " "
print(result)
```
