# Lesson 05 - Selection - Elif Statements

## Overview

An `elif` statement allows you to check additional conditions if the previous `if` or `elif` conditions were `False`.

## Syntax

The `elif` keyword adds another condition to check after an `if` statement.

* `if condition:`: The first condition that is checked.
* `elif condition:`: Another condition checked only if the previous one was `False`.
* `else:`: Runs if all previous conditions were `False`.
* Only the first `True` block runs.

```python
score = 85

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
else:
    print("Grade: Below B")
```

## Elif Before Else

All `elif` statements must come before the `else` statement.

* `if`: First condition.
* `elif`: Additional condition(s).
* `else`: Final fallback block with no condition.
* `else` must always be last.

```python
number = 0

if number > 0:
    print("Positive")
elif number == 0:
    print("Zero")
else:
    print("Negative")
```

## Order Matters With Multiple Elif

When using multiple `elif` statements, the order matters because Python stops checking once it finds the first `True` condition.

* Conditions are checked from top to bottom.
* The first `True` block runs.
* Remaining conditions are skipped.
* More specific conditions should come before broader ones.

```python
score = 95

if score >= 80:
    print("A")
elif score >= 70:
    print("B")
elif score >= 60:
    print("C")
```

## Example - Basic Usage

This program converts a numeric score into a letter grade.

```python
# Get user input and convert it to an integer
score = int(input("Enter your score: "))

# Check score ranges from highest to lowest
if score >= 80:
    print("Grade: A")
elif score >= 70:
    print("Grade: B")
elif score >= 60:
    print("Grade: C")
elif score >= 50:
    print("Grade: D")
else:
    print("Grade: F")
```

## Example - Else is Optional After Elif

This program checks a value using `if` and `elif` without an `else` block.

```python
# Assign a value
temperature = 15

# Check conditions
if temperature > 30:
    print("Hot")
elif temperature > 20:
    print("Warm")
elif temperature > 10:
    print("Cool")
```

## Example - Multiple Elif Correct and Incorrect Order

These two programs both convert a numeric score into a letter grade. The first example has the correct order. The second example has the wrong order, which causes incorrect results.

### Correct Order

This version checks higher grades first, so each score is matched correctly.

```python
# Get user input and convert it to an integer
score = int(input("Enter your score: "))

# Check highest grades first
if score >= 80:
    print("Grade: A")
elif score >= 70:
    print("Grade: B")
elif score >= 60:
    print("Grade: C")
elif score >= 50:
    print("Grade: D")
else:
    print("Grade: F")
```

### Incorrect Order

This version checks lower grades first. Because Python stops at the first `True` condition, high scores may receive the wrong grade.

```python
# Get user input and convert it to an integer
score = int(input("Enter your score: "))

# Incorrect order: lower ranges checked first
if score >= 50:
    print("Grade: D")
elif score >= 60:
    print("Grade: C")
elif score >= 70:
    print("Grade: B")
elif score >= 80:
    print("Grade: A")
else:
    print("Grade: F")
```
