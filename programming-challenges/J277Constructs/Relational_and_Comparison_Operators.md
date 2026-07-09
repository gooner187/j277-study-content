# Relational Operators

**Description:** Relational operators compare two values and produce a Boolean result of True or False, using symbols like ==, !=, >, < , >= and <=. They are the building blocks of every condition used in selection and loops.

## Example
```python
age = 15
print(age == 15)   # equal to -> True
print(age != 16)   # not equal to -> True
print(age >= 18)   # greater or equal -> False
```

# Relational / Comparison Operators — Challenges

## Challenge 1
**Type:** debug
**Difficulty:** easy
**Task:** Run the code — it returns False. Change the operator so that True is displayed. There is 1 error.
**Hint:** There are six comparison operators: ==, !=, <, >, <=, >=. Which one makes 10 compare correctly to 5 to give True?

```python
print(10 < 5)
```

## Challenge 2
**Type:** debug
**Difficulty:** easy
**Task:** Run the code — it returns False. Change the operator so that True is displayed. There is 1 error.
**Hint:** 100 is not less than 100. Think about which operators would make two equal numbers return True.

```python
print(100 < 100)
```

## Challenge 3
**Type:** debug
**Difficulty:** easy
**Task:** Run the code — it returns False. Change the operator so that True is displayed. There is 1 error.
**Hint:** != means "not equal to". 100 is not not-equal to 100 — it IS equal to 100. Which operator checks for equality?

```python
print(100 != 100)
```

## Challenge 4
**Type:** debug
**Difficulty:** medium
**Task:** Run the code — it returns False. Change the operators so that True is displayed. Both conditions use AND so both must be True individually.
**Hint:** With AND, every condition must be True for the whole expression to be True. Fix each comparison so it is individually correct.

```python
print(100 < 1 and 5 > 10)
```

## Challenge 5
**Type:** debug
**Difficulty:** medium
**Task:** Run the code — it returns False. Change the operators so that True is displayed. All three conditions use AND so all must be True.
**Hint:** Check each condition one at a time. The last one (37 >= 37) is already True — focus on fixing the first two.

```python
print(100 == 1 and 5 >= 10 and 37 >= 37)
```

## Challenge 6
**Type:** debug
**Difficulty:** medium
**Task:** Run the code — it returns False. Change the operators so that True is displayed. The conditions use OR so only one needs to be True.
**Hint:** With OR, only one condition needs to be True. You only need to fix one of the two comparisons — pick the easier one.

```python
print(100 == 1 or 100 > 100)
```

## Challenge 7
**Type:** debug
**Difficulty:** medium
**Task:** Run the code — it returns False. Change the operators so that True is displayed. There are 2 errors.
**Hint:** Think about what makes each string comparison True. Is "a" equal to "a" or not equal to "a"? Is "b" greater than or equal to "b"?

```python
print("a" != "a" and "b" >= "b")
```

## Challenge 8
**Type:** debug
**Difficulty:** hard
**Task:** Run the code — it returns False. Change the operators so that True is displayed. There are 2 errors.
**Hint:** Work out what (not False) evaluates to first — that gives you the right-hand value. Then decide what operator makes True relate correctly to that value.

```python
print("a" >= "a" and True != (not False))
```

## Challenge 9
**Type:** debug
**Difficulty:** hard
**Task:** The code should display "makes sense to me" but currently does not. Change the operators in the if condition to fix it. There are 2 errors.
**Hint:** Evaluate each part separately. What does (not False) equal? Which operator makes 5 compare correctly to 3? Which operator makes "a" compare correctly to "a"?

```python
if 5 == 3 and "a" != "a" and True >= (not False):
    print("makes sense to me")
```

## Challenge 10
**Type:** debug
**Difficulty:** hard
**Task:** The code should display "yep, i get it" but currently does not. Change the operators in the if condition to fix it. There are 2 errors.
**Hint:** Work out (not False) and (not True) separately first. Then decide what operator makes each side of AND evaluate to True.

```python
if True != (not False) and False > (not True):
    print("yep, i get it")
```
