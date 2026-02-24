# Lesson 08 - Selection - Null (`None`) Checks

## Overview

`None` represents the absence of a value. Null checks prevent your program from crashing when a variable does not contain usable data.

## The `None` Value

`None` is a special value that means “no value” or “nothing assigned.”

* `None`: A built-in constant representing no value.
* Often used as a default value.
* Different from `0`, `""`, or `False`.
* Should be checked using `is`, not `==`.

```python id="n4m8xp"
value = None

if value is None:
    print("Value has not been set")
```

## `None` Causes Errors When Not Handled Properly

If you try to use `None` like a normal value, your program can crash.

* `None` does not support arithmetic.
* `None` does not behave like a string.
* Operations on `None` often cause `TypeError`.

```python
# Assign None to a variable
number = None

# This will crash because you cannot add 5 to None
print(number + 5)
```

## When To Use `None` Checks

Null checks are especially important when:

* A variable is meant to be optional
* User input might be empty or cancelled
* Data comes from an external source
* A value is assigned later in the program

In all of these cases, assuming a value exists can cause your program to crash.

## `None` Check Syntax (use `is`)

You should check for `None` using `is` or `is not`.

* `if value is None:`: Checks if the variable contains `None`.
* `if value is not None:`: Checks if the variable contains a real value.
* `is`: Compares identity, not just equality.

```python
result = None

if result is not None:
    print("Result is:", result)
```

## Example - Basic Use

This program assigns `None` first and then checks before using the value.

```python
# Assign None to the variable
score = None

# Check before using it
if score is None:
    print("Score has not been entered yet")
```

## Example - With and Without `None` Checks

### Without a `None` Check (Crashes)

This program crashes because it tries to use `None` in arithmetic.

```python
# Ask for optional bonus points
bonus_points = None

# Attempt to calculate total score
total_score = 100 + bonus_points

print("Total score:", total_score)
```

### With a `None` Check (Safe)

This version checks for `None` before using the variable.

```python
# Ask for optional bonus points
bonus_points = None

# Check before using the value
if bonus_points is None:
    print("No bonus points were added")
else:
    total_score = 100 + bonus_points
    print("Total score:", total_score)
```
