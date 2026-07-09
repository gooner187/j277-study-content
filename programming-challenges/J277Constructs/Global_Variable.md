# Global Variable

**Description:** A global variable is declared outside all functions and can be read anywhere in the program, but a function must use the global keyword before it can change its value. Overusing them makes code harder to trace.

## Example
```python
score = 0            # global variable

def addPoint():
    global score       # needed to modify it
    score = score + 1

addPoint()
print(score)          # 1
```

# Global Variable — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure reads the global variable playerName and prints "Player: Alex". There are 3 errors — order, wrong variable name used inside and indentation.
**Hint:** A global variable declared outside a function can be read inside without the global keyword. The function must be defined before it is called. Check the variable name used in the print versus what is declared outside.

```python
showName()
playerName = "Alex"
def showName():
print("Player:", name)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Fix the code so the procedure modifies the global variable score, adding 10 each time it is called. After two calls it should print "Score: 20". There are 3 errors — missing global keyword, wrong operator and indentation.
**Hint:** To modify a global variable inside a function you must declare global score at the top of the function. Check the operator — adding points uses + not *. Fix the indentation.

```python
score = 0
def addPoints():
    score = score + 10
    print("Score:", score)
addPoints()
addPoints()
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Fix the procedure so it reduces the global lives by 1 each call, prints "Lives remaining:" or "Game over!" when lives hit 0. Three calls should print: Lives remaining: 2, Lives remaining: 1, Game over!. There are 4 errors — missing global, wrong operator, wrong comparison value and indentation.
**Hint:** Declare global lives inside the function. Losing a life means subtracting 1. Game over happens when lives == 0 not == 1. Fix the indentation of both print statements.

```python
lives = 3
def loseLife():
    lives = lives + 1
    if lives == 1:
    print("Game over!")
    else:
    print("Lives remaining:", lives)
loseLife()
loseLife()
loseLife()
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the procedure uses a for loop to add n clicks to the global totalClicks counter. After recordClicks(5) and recordClicks(3) it should print "Total clicks: 8". There are 4 errors — missing global, loop variable used instead of incrementing global, wrong range and indentation.
**Hint:** Declare global totalClicks inside the function. The loop should increment totalClicks not i. range(n) loops n times. Fix the indentation of the increment line.

```python
totalClicks = 0
def recordClicks(n):
    for i in range(n + 1):
    i += 1
recordClicks(5)
recordClicks(3)
print("Total clicks:", totalClicks)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the procedure appends a score to the global highScores list. After three calls it should print "High scores: [85, 92, 78]". There are 3 errors — missing global, wrong method name and the list not printed after the calls.
**Hint:** Even though you can append to a global list without global in some cases, it is good practice to declare it. Check the spelling of the append method. Add a print statement after the three calls.

```python
highScores = []
def addScore(score):
    highScores.apend(score)
addScore(85)
addScore(92)
addScore(78)
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so the global attempts counter increases inside the while loop. The loop should keep asking for a password up to MAX_ATTEMPTS times. After running it should print "Total attempts: 3". There are 4 errors — missing global, wrong comparison in while, attempts not incremented and indentation.
**Hint:** Declare global attempts inside the function. The while loop should run while attempts < MAX_ATTEMPTS. The input and increment must be inside the loop. Fix the indentation throughout.

```python
attempts = 0
MAX_ATTEMPTS = 3
def tryLogin():
    while attempts > MAX_ATTEMPTS:
    password = input("Enter password: ")
        if password == "kebab":
            print("Login successful")
        else:
            print("Wrong password, attempt", attempts)
tryLogin()
print("Total attempts:", attempts)
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** Fix the code so two procedures share the global gameRunning variable. checkGameOver sets it to False when lives reach 0. showStatus prints the correct message. There are 4 errors — missing global in checkGameOver, wrong comparison, missing global in showStatus (it only reads but good practice) and indentation.
**Hint:** Declare global gameRunning in checkGameOver since it modifies it. lives <= 0 should set gameRunning to False not True. Fix the indentation of the assignments inside checkGameOver.

```python
gameRunning = True
def checkGameOver(lives):
    if lives <= 0:
    gameRunning = True
    else:
    gameRunning = True
def showStatus():
    if gameRunning:
        print("Game in progress")
    else:
        print("Game over")
showStatus()
checkGameOver(0)
showStatus()
```

## Challenge 8
**Type:** write
**Difficulty:** medium
**Task:** Declare a global list called inventory = ["sword", "shield", "potion"]. Write two procedures — addItem(item) that appends to it, and removeItem(item) that removes an item if it exists or prints "not found". Call addItem("bow"), removeItem("potion") then print the inventory. Expected: ['sword', 'shield', 'bow'].
**Hint:** Use global inventory in both procedures. Use inventory.append() to add. Use if item in inventory: before removing to avoid errors. Use inventory.remove() to delete.

## Challenge 9
**Type:** write
**Difficulty:** hard
**Task:** Declare a global 2D array: leaderboard = [["Alex", 0], ["Sam", 0], ["Raj", 0]]. Write a procedure called updateScore(playerIndex, points) that uses the global keyword and adds points to the correct player's score using leaderboard[playerIndex][1]. Call updateScore(0, 50) and updateScore(2, 75) then loop through the leaderboard to print each player and their score.
**Hint:** Use global leaderboard inside the procedure. leaderboard[playerIndex][1] accesses the score column. Use += to add points. Use a for loop after the calls to print each row.

## Challenge 10
**Type:** write
**Difficulty:** hard
**Task:** Declare three global variables: score = 0, lives = 3, level = 1. Write three procedures — collectCoin() that adds 10 to score and increases level when score reaches 30, hitEnemy() that reduces lives by 1 and prints lives left, and showStatus() that prints all three globals. Call collectCoin() three times, hitEnemy() once then showStatus(). Expected output includes "Level up! Now on level 2" and "Score: 30 | Lives: 2 | Level: 2".
**Hint:** Each procedure that modifies a global must declare it with global. collectCoin modifies both score and level — declare both. Use an if statement inside collectCoin to check if score >= 30.
