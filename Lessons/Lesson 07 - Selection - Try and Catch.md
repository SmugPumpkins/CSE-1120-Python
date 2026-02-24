# Lesson 07 - Selection - Try and Catch

## Overview

`try` and `except` allow your program to safely handle errors that would normally crash it.

### Common Invalid Inputs to Think About

When asking for user input, ask yourself:

* What if the user types letters instead of numbers?
* What if they press Enter without typing anything?
* What if they type a negative number or a decimal?
* What if they copy-paste something unexpected?
* What if they misunderstand the prompt?

At this level of computer science, the possible errors that could show up are **all preventable**. Your code should be able to handle **any kind of error that it encounters** because we are working with limited amounts and types of data.

## Syntax

A `try` block contains code that might cause an error. An `except` block handles the error if it occurs.

* `try:`: Starts a block of code that may fail.
* Indented code: The code that could cause an exception.
* `except ExceptionType:`: Catches a specific type of error.
* Indented block under `except`: Runs only if that error happens.

```python id="v7e92m"
try:
    number = int(input("Enter a number: "))
    print("You entered:", number)
except ValueError:
    print("That was not a valid integer.")
```

## Exceptions

An exception is an error that occurs while a program is running.

### Generic Exception

A generic `Exception` catches any type of error. It is broad and should be used carefully.

* `except Exception:`: Catches all exceptions.
* Useful when you want to prevent any crash.
* Less specific than catching a named error.

```python
try:
    value = int("hello")
except Exception:
    print("Something went wrong.")
```

### ValueError

A `ValueError` happens when a function receives the correct type but an invalid value.

* `int("abc")`: Causes a `ValueError` because `"abc"` cannot be converted to an integer.
* `except ValueError:`: Handles invalid numeric input.

```python
try:
    number = int(input("Enter a whole number: "))
except ValueError:
    print("You must enter a valid whole number.")
```

### TypeError

A `TypeError` happens when an operation is performed on an inappropriate type.

* `"5" + 5`: Causes a `TypeError` because you cannot add a string and an integer.
* `except TypeError:`: Handles type mismatch errors.

```python
try:
    result = "5" + 5
except TypeError:
    print("You cannot add a string and an integer.")
```

## Try / Except vs If / Else

| `if` / `else`                              | `try` / `except`                                  |
| ------------------------------------------ | ------------------------------------------------- |
| You can check the condition ahead of time. | You cannot know in advance if the code will fail. |
| You are comparing values.                  | You are converting input or accessing data.       |

## Example - Basic Usage

This program safely converts user input into an integer.

```python
# Ask the user for input
user_input = input("Enter a number: ")

try:
    # Attempt to convert input to an integer
    number = int(user_input)
    print("Double your number is:", number * 2)
except ValueError:
    # This runs if conversion fails
    print("Invalid input. Please enter a whole number.")
```

## Example - Common Cases With User Input

### Example 1 – Handling Letters Instead of Numbers

```python
# Ask the user for their age
age_input = input("Enter your age: ")

try:
    # Attempt conversion
    age = int(age_input)
    print("Next year you will be:", age + 1)
except ValueError:
    # Handle invalid numeric input
    print("Age must be a whole number.")
```

### Example 2 – Handling Negative Numbers

```python
# Ask for a positive number
number_input = input("Enter a positive number: ")

try:
    number = int(number_input)

    # Check logical validity after conversion
    if number < 0:
        print("Number must not be negative.")
    else:
        print("Valid number entered.")
except ValueError:
    print("That is not a valid whole number.")
```

### Example 3 – Catching Multiple Types of Errors

```python
# Ask the user for a number
user_input = input("Enter a number to divide 100 by: ")

try:
    number = int(user_input)

    # Attempt division
    result = 100 / number
    print("Result:", result)

except ValueError:
    # Handles invalid integer conversion
    print("Please enter a valid whole number.")
except ZeroDivisionError:
    # Handles division by zero
    print("You cannot divide by zero.")
```
