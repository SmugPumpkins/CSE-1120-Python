# Lesson 03 - Selection - Logical Keywords

## Overview

Logical keywords allow you to combine, modify, and evaluate multiple conditions inside an `if` statement.

## `and`

The `and` keyword requires both conditions to be `True` for the entire expression to be `True`.

* `age >= 18`: First condition being checked.
* `score > 80`: Second condition being checked.
* `and`: Both conditions must be `True`.
* The indented block runs only if both comparisons are `True`.

```python
age = 20
score = 90

if age >= 18 and score > 80:
    print("You qualify")
```

## `or`

The `or` keyword requires at least one condition to be `True` for the entire expression to be `True`.

* `temperature < 0`: First condition.
* `temperature > 30`: Second condition.
* `or`: Only one condition needs to be `True`.
* The block runs if either comparison is `True`.

```python
temperature = -5

if temperature < 0 or temperature > 30:
    print("Extreme temperature detected")
```

### Exclusive Or with `^`

The `^` operator (exclusive or) returns `True` only when exactly one condition is `True`.

* `True ^ False`: Evaluates to `True` because only one value is `True`.
* `True ^ True`: Evaluates to `False` because both are `True`.
* `a > 0 ^ b > 0`: Only one comparison can be `True`.

```python
a = 5
b = -3

if (a > 0) ^ (b > 0):
    print("Exactly one value is positive")
```

## `not`

The `not` keyword reverses a boolean value.

* `logged_in = False`: Assigns a boolean value.
* `not logged_in`: Flips `False` to `True`.
* The block runs because `not False` becomes `True`.

```python
logged_in = False

if not logged_in:
    print("Please log in")
```

## Brackets and Order of Operations with Logical Keywords

Parentheses control the order in which logical expressions are evaluated.

* `(a > 0 and b > 0)`: Evaluates this group first.
* `or c > 0`: Evaluated after the grouped expression.
* Parentheses change how conditions are combined.

```python
a = 5
b = -2
c = 3

if (a > 0 and b > 0) or c > 0:
    print("The overall condition is True")
```

## `is`

The `is` keyword checks whether two variables refer to the same object in memory.

* `x = None`: Assigns the special value `None`.
* `x is None`: Checks identity, not equality.
* The block runs if `x` is exactly `None`.

```python
x = None

if x is None:
    print("x has no value assigned")
```

## `in`

The `in` keyword checks whether a value exists inside a sequence such as a string or list.

* `"a" in "apple"`: Checks if the character exists in the string.
* `3 in numbers`: Checks if the value exists in the list.
* The block runs if the value is found.

```python
numbers = [1, 2, 3, 4]

if 3 in numbers:
    print("3 is in the list")
```

## Example - Basic Usage

This program uses `and` and `not` to check multiple conditions.

```python
# Assign values
age = 22
has_id = True
banned = False

# Check multiple conditions
if age >= 18 and has_id and not banned:
    print("You may enter")
```

## Example - Different Brackets, Different Results

This program shows how parentheses change how conditions are evaluated.

```python
# Assign values
a = 5
b = 10
c = -1

# First condition with one grouping
if a > 0 and (b > 0 or c > 0):
    print("First condition is True")

# Second condition with different grouping
if (a > 0 and b > 0) or c > 0:
    print("Second condition is True")
```

## Example - `and` vs Nesting

This program compares using `and` in one condition versus nested `if` statements.

```python
# Assign values
age = 19
score = 85

# Using and
if age >= 18 and score > 80:
    print("Qualified using and")

# Using nested if statements
if age >= 18:
    if score > 80:
        print("Qualified using nesting")
```

## Example - `in` With Lists

This program checks whether a value exists inside a list.

```python
# Create a list of names
names = ["Alice", "Bob", "Charlie"]

# Check if a name is in the list
if "Bob" in names:
    print("Bob is on the list")
```
