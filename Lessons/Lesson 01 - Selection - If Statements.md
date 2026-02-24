# Lesson 01 - Selection - If Statements

## Overview

An `if` statement allows a program to make decisions by running code only when a specific condition is `True`.

## Syntax

An `if` statement checks a condition and runs an indented block of code only if that condition evaluates to `True`.

* `if`: The keyword that starts the conditional statement.
* `5 > 3`: A `condition`, an expression that evaluates to `True` or `False`.
* `:`: A colon that marks the start of the indented block.
* Indented code: The block that runs only when the condition is `True`.

```python
if 5 > 3:
    print("Five is greater than three")
```

### Indentation

Indentation defines which lines of code belong to the `if` statement.

* `if 10 > 5:`: The condition being checked.
* `:`: Indicates that an indented block follows.
* `    print(...)`: Four spaces show this line is inside the `if` block.

```python
if 10 > 5:
    print("This line is inside the if statement")
print("This line is outside the if statement")
```

### `pass`

The `pass` statement is used when an `if` block is required syntactically, but you do not want it to do anything yet.

* `if True:`: A condition that always evaluates to `True`.
* `pass`: A placeholder that does nothing but prevents an error.

```python
if True:
    pass
```

### Assignment `=` vs Comparison `==`

`=` assigns a value to a variable, while `==` compares two values to check if they are equal.

* `number = 5`: Assigns the value `5` to the variable `number`.
* `number == 5`: Checks whether `number` is equal to `5`.
* `if number == 5:`: Runs the block only if the comparison is `True`.

```python
number = 5

if number == 5:
    print("The number is five")
```

The code below will result in an error because it is using assignment instead of comparing the values:

```python
number = 5

if number = 5:
    print("The number is five")
```

## Conditions Evaluate to `True` or `False`

Every condition in an `if` statement evaluates to either `True` or `False`.

### Code Runs When Condition is `True`

When the condition evaluates to `True`, the indented block executes.

* `age = 18`: Assigns a value to the variable.
* `if age >= 18:`: Checks whether `age` is greater than or equal to 18.
* Indented `print(...)`: Runs only if the condition is `True`.

```python
age = 18

if age >= 18:
    print("You are an adult")
```

### Code Does Not Run When Condition is `False`

When the condition evaluates to `False`, the indented block is skipped.

* `temperature = 10`: Assigns a value to the variable.
* `if temperature > 20:`: Checks whether `temperature` is greater than 20.
* Indented `print(...)`: Will not run because the condition is `False`.

```python
temperature = 10

if temperature > 20:
    print("It is warm outside")
```

## Example - Basic Use

This program checks whether a number is positive and prints a message only if the condition is `True`.

```python
# Assign a value to the variable
number = 7

# Check if the number is greater than zero
if number > 0:
    # This line runs only if the condition is True
    print("The number is positive")
```

## Example - Some Code Runs, Some Does Not

This program shows that only the code inside a `True` condition runs, while code inside a `False` condition is skipped.

```python
# Assign values to variables
score = 90
level = 3

# This condition is True, so this block runs
if score > 50:
    print("You passed the test")

# This condition is False, so this block does not run
if level > 5:
    print("You unlocked the next level")

# This line always runs because it is outside any if statement
print("Program complete")
```

## Example - Nested If Statement

This program demonstrates an `if` statement inside another `if` statement. The inner block only runs if both conditions are `True`.

```python
# Assign values to variables
age = 20
has_ticket = True

# Outer if statement checks age
if age >= 18:
    print("You are old enough to enter")

    # Inner if statement checks ticket status
    if has_ticket == True:
        print("You may enter the event")
```
