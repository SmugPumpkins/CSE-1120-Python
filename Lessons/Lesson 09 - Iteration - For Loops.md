# Lesson 09 - Iteration - For Loops

## Overview

A `for` loop is used to repeat a block of code a specific number of times or once for each item in a sequence.

## Syntax

A `for` loop runs code for each value in a sequence such as `range()`.

* `for`: The keyword that starts the loop.
* `variable`: Stores the current value during each loop iteration.
* `in`: Connects the variable to the sequence.
* `range()`: Generates a sequence of numbers.
* `:`: Starts the indented loop block.
* Indented code: Runs once for each value.

```python id="f3k9zp"
for i in range(5):
    print(i)
```

## When You Use `i` In The Loop

You use the loop variable (commonly `i`) when you need the current number in each iteration.

* `i`: Stores the current number from `range()`.
* `range(5)`: Produces numbers 0 through 4.
* `print(i)`: Uses the loop variable inside the loop.

```python
for i in range(5):
    print("Current value:", i)
```

## When You Don't Need the `i` Value

If you do not need the loop variable, use `_` as a placeholder.

* `_`: A common placeholder variable name.
* `range(3)`: Runs the loop three times.
* The value is ignored.

```python
for _ in range(3):
    print("Hello")
```

## `range()` With 2 Parameters

When `range()` has two parameters, it starts at the first value and stops before the second.

* `range(start, stop)`: Generates numbers from `start` up to (but not including) `stop`.
* `range(2, 6)`: Produces 2, 3, 4, 5.
* The stop value is not included.

```python
for i in range(2, 6):
    print(i)
```

## `range()` With 3 Parameters

When `range()` has three parameters, the third controls the step size.

* `range(start, stop, step)`: Moves by `step` each time.
* `range(0, 10, 2)`: Produces 0, 2, 4, 6, 8.
* Step controls how much the number increases (or decreases).

```python
for i in range(0, 10, 2):
    print(i)
```

## Example - Basic Use

This program prints numbers from 1 to 5.

```python
# Loop from 1 up to (but not including) 6
for i in range(1, 6):
    print(i)
```

## Example - `Range` With Multiple Parameters

This program prints even numbers from 2 to 20.

```python
# Loop from 2 up to 21, stepping by 2
for i in range(2, 21, 2):
    print(i)
```

## Example - Nested For Loop

This program demonstrates a `for` loop inside another `for` loop.

```python
# Outer loop runs 3 times
for i in range(3):
    print("Outer loop:", i)

    # Inner loop runs 2 times for each outer iteration
    for j in range(2):
        print("  Inner loop:", j)
```
