# Lesson 04 - Selection - Else Statements

## Overview

An `else` statement runs a block of code when the `if` condition evaluates to `False`.

## Syntax

An `else` block is attached directly to an `if` statement and runs only when the `if` condition is `False`.

* `if condition:`: Checks whether the condition is `True`.
* Indented block under `if`: Runs when the condition is `True`.
* `else:`: Must align with the `if` and has no condition.
* Indented block under `else`: Runs when the `if` condition is `False`.

```python
number = 4

if number > 5:
    print("Number is greater than five")
else:
    print("Number is five or less")
```

## Example - Basic Usage

This program checks whether a number is positive. If it is not, the `else` block runs instead.

```python
# Assign a value to the variable
number = -3

# Check if the number is greater than zero
if number > 0:
    # This runs if the condition is True
    print("The number is positive")
else:
    # This runs if the condition is False
    print("The number is zero or negative")
```

## Example - If / Else With Strings

This program compares a string value and uses `else` to handle the opposite case.

```python
# Assign a value to the variable
password = "python123"

# Check if the password matches
if password == "python123":
    # This runs if the strings are equal
    print("Access granted")
else:
    # This runs if the strings are not equal
    print("Access denied")
```
