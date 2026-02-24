# Lesson 06 - Selection - Match Case

## Overview

The `match` statement allows you to compare one value against multiple possible patterns in a clean and structured way.

## Syntax

A `match` statement checks a value and runs the first `case` that matches.

* `match value:`: The value being checked.
* `case pattern:`: A possible match for that value.
* Indented block: Runs if the pattern matches.
* Only the first matching case executes.

```python
number = 3

match number:
    case 1:
        print("One")
    case 2:
        print("Two")
    case 3:
        print("Three")
```

## Default Value

The underscore `_` acts as a default case when no other patterns match.

* `case _:`: Matches anything not previously matched.
* Works like an `else` statement.
* Should appear last.

```python
color = "purple"

match color:
    case "red":
        print("Red selected")
    case "blue":
        print("Blue selected")
    case _:
        print("Unknown color")
```

## Order Matters

`match` checks cases from top to bottom and stops at the first match.

* Cases are evaluated in order.
* The first matching case runs.
* More specific cases should come before broader ones.
* A broad case placed first can prevent others from running.

```python
value = 10

match value:
    case 10:
        print("Exactly ten")
    case _:
        print("Something else")
```

## Example - Basic Usage

This program asks the user for a number and prints a matching message.

```python
# Get user input and convert it to an integer
number = int(input("Enter a number (1-3): "))

# Match the number
match number:
    case 1:
        print("You chose one")
    case 2:
        print("You chose two")
    case 3:
        print("You chose three")
    case _:
        print("Invalid choice")
```

## Example - Days of the Week

This program checks a string representing a day of the week and prints whether it is a weekday or weekend.

```python
# Get user input and convert it to lowercase
day = input("Enter a day of the week: ").lower()

# Match the day string
match day:
    case "monday":
        print("Weekday")
    case "tuesday":
        print("Weekday")
    case "wednesday":
        print("Weekday")
    case "thursday":
        print("Weekday")
    case "friday":
        print("Weekday")
    case "saturday":
        print("Weekend")
    case "sunday":
        print("Weekend")
    case _:
        print("Not a valid day")
```

## Example - Correct and Incorrect Order

These two programs both convert a numeric score into a letter grade using `match`. The first example uses correct ordering. The second example uses incorrect ordering, which causes incorrect results.

### Correct Order

This version places the most specific conditions first.

```python
# Get user input and convert it to an integer
score = int(input("Enter your score: "))

# Match score ranges using guards
match score:
    case s if s >= 90:
        print("Grade: A")
    case s if s >= 80:
        print("Grade: B")
    case s if s >= 70:
        print("Grade: C")
    case s if s >= 60:
        print("Grade: D")
    case _:
        print("Grade: F")
```

### Incorrect Order

This version checks lower ranges first. Because `match` stops at the first match, higher scores receive the wrong grade.

```python
# Get user input and convert it to an integer
score = int(input("Enter your score: "))

# Incorrect order: lower ranges checked first
match score:
    case s if s >= 60:
        print("Grade: D")
    case s if s >= 70:
        print("Grade: C")
    case s if s >= 80:
        print("Grade: B")
    case s if s >= 90:
        print("Grade: A")
    case _:
        print("Grade: F")
```
