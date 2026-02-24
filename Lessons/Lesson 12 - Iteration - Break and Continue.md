# Lesson 12 - Iteration - Break and Continue

## Overview

`break` and `continue` are used inside loops to control how and when iterations stop or skip.

## `break` Syntax

The `break` statement immediately stops the loop entirely.

* `break`: Ends the loop immediately.
* Used inside `for` or `while` loops.
* The loop does not continue after `break` runs.
* Execution moves to the first line after the loop.

```python id="b8k3wp"
for i in range(5):
    if i == 3:
        break
    print(i)
```

## `continue` Syntax

The `continue` statement skips the rest of the current iteration and moves to the next one.

* `continue`: Skips the remaining code in the current loop iteration.
* The loop does not stop completely.
* The next iteration begins immediately.

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

## Example - Basic Usage

This program demonstrates both `break` and `continue` in a simple loop.

```python
# Loop through numbers 0 to 4
for i in range(5):

    # Skip the number 1
    if i == 1:
        continue

    # Stop the loop when i is 4
    if i == 4:
        break

    print(i)
```

## Example - Ending an Infinite Loop

This program uses `break` to safely end what would otherwise be an infinite loop.

```python
# Start an infinite loop
while True:

    # Ask for user input
    user_input = input("Type 'exit' to quit: ")

    # Stop the loop if user types exit
    if user_input == "exit":
        break

    print("You typed:", user_input)
```

## Example - Ending a Search Early

This program searches a list and stops once the item is found.

```python
# Create a list
numbers = [4, 8, 15, 16, 23, 42]

# Search for a specific value
for number in numbers:

    if number == 15:
        print("Number found!")
        break

    print("Checking:", number)
```

## Example - Skipping Elements in a For Loop

This program skips even numbers and prints only odd numbers.

```python
# Loop from 1 to 10
for i in range(1, 11):

    # Skip even numbers
    if i % 2 == 0:
        continue

    print(i)
```
