# Lesson 10 - For Loops With Iterables

## Overview

A `for` loop can iterate directly over items in a collection such as a string, list, tuple, or dictionary.

## What Is an Iterable?

An iterable is any object that can return its elements one at a time.

* Common iterables include `str`, `list`, `tuple`, and `dict`.
* A `for` loop retrieves one item per iteration.
* You do not need `range()` when looping over an iterable.

```python id="k92mdp"
numbers = [10, 20, 30]

for number in numbers:
    print(number)
```

## Syntax

A `for` loop assigns each item in the iterable to a variable during each iteration.

* `for item in iterable:`: Loops through each element.
* `item`: Stores the current value.
* `iterable`: The collection being looped over.
* Indented block: Runs once for each item.

```python
colors = ["red", "green", "blue"]

for color in colors:
    print(color)
```

## Enumerate

`enumerate()` gives you both the index and the value while looping.

* `enumerate(iterable)`: Wraps the iterable and adds an index counter.
* `index`: The current position.
* `value`: The current item.
* Useful when you need both position and data.

```python
names = ["Alice", "Bob", "Charlie"]

for index, name in enumerate(names):
    print(index, name)
```

## Example - Basic Usage

This program loops over a list and prints each item.

```python
# Create a list
items = ["pen", "pencil", "paper"]

# Loop through each item
for item in items:
    print(item)
```

## Example - `str`

This program loops through each character in a string.

```python
# Define a string
word = "Python"

# Loop through each character
for letter in word:
    print(letter)
```

## Example - `list`

This program loops through a list of numbers.

```python
# Create a list
numbers = [1, 2, 3, 4]

# Loop through the list
for number in numbers:
    print("Number:", number)
```

## Example - `tuple`

This program loops through a tuple.

```python
# Create a tuple
coordinates = (10, 20, 30)

# Loop through the tuple
for value in coordinates:
    print("Value:", value)
```

## Example - `dict`

This program loops through a dictionary.

```python
# Create a dictionary
student = {
    "name": "Alice",
    "grade": 90
}

# Loop through dictionary keys
for key in student:
    print("Key:", key)
    print("Value:", student[key])
```

## Example - Enumerate

This program uses `enumerate()` to show index positions along with values.

```python
# Create a list
fruits = ["apple", "banana", "cherry"]

# Loop with index and value
for index, fruit in enumerate(fruits):
    print("Index:", index)
    print("Fruit:", fruit)
```

## Example - For Loop For Related Iterables

This program loops through two related lists using their index.

```python
# Create two related lists
names = ["Alice", "Bob", "Charlie"]
scores = [85, 92, 78]

# Loop using index to access both lists
for i in range(len(names)):
    print("Name:", names[i])
    print("Score:", scores[i])
```
