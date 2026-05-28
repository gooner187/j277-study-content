# Basic File Handling — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it opens and displays the contents of poem.txt. There is 1 error — a typo in the open function name. Create a poem.txt tab using the + button and add the poem content shown below.
**Hint:** The function to open a file is open() — check the spelling carefully.
**File: poem.txt**
```
Roses are red,
Violets are blue,
Python is awesome,
And so are you!
```

```python
holder = opeen("poem.txt", "r")
print(holder.read())
holder.close()
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it opens, reads and properly closes poem.txt. There is 1 error — a typo in the close method. Create a poem.txt tab with the poem content.
**Hint:** The method to close a file is close() — check the spelling carefully.
**File: poem.txt**
```
Roses are red,
Violets are blue,
Python is awesome,
And so are you!
```

```python
holder = open("poem.txt", "r")
print(holder.read())
holder.cllose()
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it reads and displays poem.txt correctly. There are 2 errors — the wrong file method is used for reading and the close statement is incomplete.
**Hint:** To read a file use .read() not .write(). The close statement needs brackets () at the end to actually call the method.
**File: poem.txt**
```
Roses are red,
Violets are blue,
Python is awesome,
And so are you!
```

```python
holder = open("poem.txt", "r")
print(holder.write())
holder.close
```

## Challenge 4
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so it opens readThis.txt, takes user input and writes it to the file. There are 2 errors — a variable name case mismatch and a missing bracket on close.
**Hint:** Python is case sensitive — usercontent and userContent are different variable names. close() needs opening and closing brackets to work.

```python
notepad = open("readThis.txt", "w")
userContent = input("Type something>>>")
notepad.write(usercontent)
notepad.close)
```

## Challenge 5
**Type:** extend
**Difficulty:** easy
**Task:** Run the code and observe the difference between readline() (one line) and readlines() (all remaining lines as a list). Then edit the code so it only displays the first two lines of the poem — remove the readlines() line.
**Hint:** Each call to readline() reads the next line. Remove the last print statement to stop after two lines.
**File: poem.txt**
```
Roses are red,
Violets are blue,
Python is awesome,
And so are you!
```

```python
holder = open("poem.txt", "r")
print(holder.readline())
print(holder.readline())
print(holder.readlines())
holder.close()
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so it opens poem.txt and displays it one line at a time using a while loop and readline(). The loop stops when an empty line is read. There are 4 errors.
**Hint:** Files are opened with open() not input(). Check the spelling of readline. The close method should be called on the file variable not on loop. The closing bracket of close() should be ) not }.
**File: poem.txt**
```
Roses are red,
Violets are blue,
Python is awesome,
And so are you!
```

```python
holdPoem = input("poem.txt", "r")
loop = True
while loop == True:
  oneLinefromPoem = holdPoem.readliine()
  print(oneLinefromPoem)
  if oneLinefromPoem == "":
    loop = False

loop.close(}
```

## Challenge 7
**Type:** extend
**Difficulty:** easy
**Task:** The code creates a file and asks for input but does not save anything to it. Add the two missing lines so the user input is written to the file and the file is properly closed.
**Hint:** Use notepad.write(userContent) to write the input to the file. Use notepad.close() to close it. Both lines go after the input line.

```python
notepad = open("readThis.txt", "w")
userContent = input("Type something>>>")
```

## Challenge 8
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so it writes three lines to a file using writelines(). There are 3 errors — a missing closing quote in open(), a variable name typo and a wrong escape character in the third string.
**Hint:** The open mode "w" needs a closing speech mark. Check the variable name used in writelines() — does it match what was declared? The newline character is \n not \m.

```python
file = open("writelines_example.txt", "w)
multiplLines = ["Hello, world!\n", "This is the second line.\n", "This is the third line.\m"]
fille.writelines(multiplLines)
file.close()
```

## Challenge 9
**Type:** write
**Difficulty:** medium
**Task:** Write a program that opens a file called "notes.txt" in write mode, asks the user to type some text, writes it to the file, closes the file, then opens it again in read mode and displays the contents back to the user.
**Hint:** Open with "w" to write, close it, then open again with "r" to read. Use input() to get the text and .write() to save it. Use .read() to display it.

## Challenge 10
**Type:** write
**Difficulty:** medium
**Task:** Create a text file tab called "data.txt" and add at least 3 lines of your own text. Write Python code that opens the file, reads and displays all the content, then closes the file.
**Hint:** Use open("data.txt", "r") to open in read mode. Use .read() to get all contents or .readlines() to get a list of lines. Always close the file with .close().
