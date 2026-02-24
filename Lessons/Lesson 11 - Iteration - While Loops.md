# Lesson 11 - Iteration - While Loops

## Overview

A `while` loop repeatedly runs a block of code as long as a condition remains `True`.

## Syntax

A `while` loop checks a condition before each iteration.

* `while`: The keyword that starts the loop.
* `condition`: An expression that evaluates to `True` or `False`.
* `:`: Starts the indented loop block.
* Indented code: Runs repeatedly while the condition is `True`.
* The condition must eventually become `False` to stop the loop.

```python id="w3m9ql"
count = 0

while count < 3:
    print(count)
    count += 1
```

## The `while` Condition

The condition controls how long the loop runs.

* The condition is checked before each iteration.
* If the condition is `True`, the loop runs.
* If the condition is `False`, the loop stops.
* You must update a variable inside the loop to avoid infinite loops.

```python
number = 5

while number > 0:
    print(number)
    number -= 1
```

## Example - Basic Use

This program counts from 1 to 5 using a `while` loop.

```python
# Start value
counter = 1

# Loop while counter is less than or equal to 5
while counter <= 5:
    print(counter)

    # Increase counter each time
    counter += 1
```

## Example - Recreating a For Loop With `while`

This program recreates a simple `for` loop using a `while` loop.

```python
# Initialize the loop variable
i = 0

# Loop while i is less than 5
while i < 5:
    print(i)

    # Update the loop variable
    i += 1
```

## Example - Infinite Loop

This program creates an infinite loop because the condition never becomes `False`.

```python
# This loop never changes the condition
while True:
    print("This will run forever")
```
