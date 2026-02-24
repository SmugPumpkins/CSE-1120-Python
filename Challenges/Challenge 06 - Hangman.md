# Challenge 06 - Hangman
The object of this challenge is to

## Mild 🌶️
Create a program that satisfies the following requirements:

* The program has a preselected word chosen by the programmer.
* The user guesses single characters.
* The user gets 15 guesses to guess the word.
* The program prints 3 things between each guess:
    * The incorrect characters or words guessed so far.
    * The blanks for the word, with correct guesses added to the correct places (if the user has made correct guesses)
        * e.g. `_ e _ _ o  _ o _ _ d`
    * The number of remaining guesses.
* The program prevents the user from typing invalid values and handles errors appropriately.
* The program only moves forward if input is valid.

## Medium 🌶️🌶️
Create a program that satisfies the following requirements:

* The program has a preselected word chosen by the programmer.
* The user guesses single characters.
* The user has as many guesses as they want, but the game ends if they get 6 incorrect guesses.
* The program prints 3 things between each guess:
    * The incorrect characters or words guessed so far.
    * The blanks for the word, with correct guesses added to the correct places (if the user has made correct guesses)
        * e.g. `_ e _ _ o  _ o _ _ d`
    * The number of remaining incorrect guesses.
* The program prevents the user from typing invalid values and handles errors appropriately.
* The program only moves forward if input is valid.

## Spicy 🌶️🌶️🌶️
Create a program that satisfies the following requirements:

* The program has a list of at least 3 words selected by the programmer that it chooses from randomly.
* The user guesses single characters.
* The user has as many guesses as they want, but the game ends if they get 6 incorrect guesses.
* The program prints 3 things between each guess:
    * The incorrect characters or words guessed so far.
    * The blanks for the word, with correct guesses added to the correct places (if the user has made correct guesses)
        * e.g. `_ e _ _ o  _ o _ _ d`
    * The ascii art of the current state of the hangman (ascii art is provided below)
* The program prevents the user from typing invalid values and handles errors appropriately.
* The program only moves forward if input is valid.

## Hangman Ascii Art

```
"""
  +---+
  |   |
      |
      |
      |
      |
=========
"""
```
```
"""
 +---+
  |   |
  O   |
      |
      |
      |
=========
"""
```
```
"""
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
"""
```
```
"""
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========
"""
```
```
"""
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
"""
```
```
"""
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
"""
```
```
"""
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
"""
```