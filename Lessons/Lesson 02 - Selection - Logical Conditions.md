# Lesson 02 - Selection - Logical Comparisons

## Overview

Logical comparison operators are used in `if` statements to compare values and produce either `True` or `False`.

## Equality `==`

The equality operator checks whether two values are the same.

* `==`: Compares two values.
* `5 == 5`: Evaluates to `True` because both values are equal.
* `if 5 == 5:`: Runs the indented block only if the comparison is `True`.

```python
if 5 == 5:
    print("The values are equal")
```

## Inequality `!=`

The inequality operator checks whether two values are different.

* `!=`: Compares two values to see if they are not equal.
* `5 != 3`: Evaluates to `True` because the values are different.
* `if 5 != 3:`: Runs the indented block only if the comparison is `True`.

```python
if 5 != 3:
    print("The values are not equal")
```

## Greater Than `>` and Greater Than or Equal `>=`

These operators compare whether one value is larger than another.

* `>`: Checks if the value on the left is greater than the value on the right.
* `>=`: Checks if the value on the left is greater than or equal to the value on the right.
* `if score > 70:`: Runs if `score` is strictly greater than 70.
* `if score >= 70:`: Runs if `score` is 70 or higher.

```python
score = 85

if score > 70:
    print("Score is greater than 70")

if score >= 85:
    print("Score is at least 85")
```

## Less Than `<` and Less Than or Equal `<=`

These operators compare whether one value is smaller than another.

* `<`: Checks if the value on the left is less than the value on the right.
* `<=`: Checks if the value on the left is less than or equal to the value on the right.
* `if temperature < 0:`: Runs if `temperature` is below 0.
* `if temperature <= 0:`: Runs if `temperature` is 0 or lower.

```python
temperature = -2

if temperature < 0:
    print("Temperature is below freezing")

if temperature <= -2:
    print("Temperature is at or below -2")
```

## Example - Basic Use

This program compares two numbers and prints a message when the condition is `True`.

```python
# Assign values to variables
a = 10
b = 20

# Check if a is less than b
if a < b:
    print("a is less than b")
```

## Example - Some Code Runs, Some Does Not

This program shows that only `True` comparisons run their indented blocks.

```python
# Assign values to variables
points = 50
lives = 3

# This condition is True, so this block runs
if points >= 50:
    print("You reached the minimum points")

# This condition is False, so this block does not run
if lives > 5:
    print("You have many lives left")

# This line always runs because it is outside any if statement
print("Game over")
```

## Example - Nested If Statements

This program demonstrates one `if` statement inside another. The inner block only runs if both comparisons are `True`.

```python
# Assign values to variables
age = 25
score = 90

# First condition checks age
if age >= 18:
    print("You are an adult")

    # Second condition checks score
    if score > 80:
        print("You earned a high score")
```
