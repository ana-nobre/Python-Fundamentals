# Python Mini-Games -- Quiz & Word Guessing (Jupyter Notebook)

This repository contains two simple Python games built as learning
projects:\
1. **Geography Quiz Game**\
2. **Hangman Game**

Both are designed to practice core Python concepts using **Jupyter
Notebook**.

------------------------------------------------------------------------

# 🌍 Geography Quiz Game

A quiz game about **geography questions**, built in Python.\
The player has a limited number of attempts to answer correctly.

## 📌 Overview

-   The game asks random geography questions.\
-   The player must answer correctly to score points.\
-   **Winning condition**: 5 correct answers.\
-   **Losing condition**: 3 incorrect answers.

## 🧠 Python Concepts Used

-   Dictionaries (storing question → answer pairs)\
-   Randomness (`random.choice` to pick a question)\
-   Input/output (`input()`, `print()`)\
-   Control flow (`if/elif/else`)\
-   Loops (`while` loop to keep asking questions)\
-   Counters (track correct and incorrect answers)\
-   Functions (to reuse game logic with different sets of questions)

## 🕹️ Example Questions

1.  On which continent is Mount Everest located? → **Asia**\
2.  On which continent can you see the most penguins? → **Antarctica**\
3.  In which country is the Eiffel Tower located? → **France**\
4.  Berlin is the capital of? → **Germany**\
5.  From which country do the Samurais come? → **Japan**\
6.  Where would you go if you wanted to see kangaroos? → **Australia**\
7.  n which continent is the Amazon Rainforest mainly located? → **South America**\
8.  In which country is it a tradition to paint your face on the Day of
    the Dead? → **Mexico**\

## 💻 Code Examples (Key Concepts)

### Dictionary of Questions

``` python
quiz = {
    "On which continent is Mount Everest located?": "Asia",
    "What is the largest country in the Americas?": "Canada",
    "On which continent can you see the most penguins?": "Antarctica",
    "In which country is the Eiffel Tower located?": "France",
    "Berlin is the capital of?": "Germany",
    "From which country do the Samurais come?": "Japan",
    "Where would you go if you wanted to see kangaroos?": "Australia",
    "On which continent is the Sahara Desert located?": "Africa",
    "In which country is it a tradition to paint your face on the Day of the Dead?": "Mexico",
    "Tikka Masala is a traditional dish from...?": "India",
    "On which continent is the Amazon Rainforest mainly located?": "South America"
}
```

### While Loop with Win/Lose Conditions

``` python
while correct < 5 and wrong < 3:
    question = random.choice(list(quiz.keys()))
    answer = quiz[question]
    choice = input(question + " ")

    if choice == answer:
        correct += 1
        print("Correct!")
    else:
        wrong += 1
        print("Wrong!")
```

### Encapsulating in a Function (simplified)

``` python
def quiz_game(questions_dict):
    # Same logic wrapped in a function
    # so it can be reused with any set of Q&A
    ...
```

------------------------------------------------------------------------

# 🔤 Word Guessing Game

A classic word-guessing game where one player chooses a secret word and
the other tries to guess it before running out of attempts.

## 📌 Overview

-   One player chooses a secret word.\
-   The guessing player tries to guess letters.\
-   Correct guesses reveal the letters in place.\
-   Incorrect guesses reduce the number of attempts and draw the
    hangman.\
-   **Winning condition**: Guess the word before attempts run out.\
-   **Losing condition**: Run out of attempts before guessing the word.

## 🧠 Python Concepts Used

-   Strings and lists (managing the secret word and underscores)\
-   Loops (`while`)\
-   Conditionals (`if/elif/else`)\
-   String methods (`.lower()`, `.capitalize()`)\
-   User input validation\
-   Game state tracking (remaining attempts, guessed letters)

## 💻 Code Example (simplified)

``` python
while attempts != 0:
    guess = input('Enter a letter or the full secret word: ').lower()

    if guess == secret_word:
        print(f'You guessed it! The secret word was: {secret_word}')
        break
    elif guess in secret_word:
        hidden_word[secret_word.index(guess)] = guess
        print(' '.join(hidden_word))
        continue
    else:
        attempts -= 1
        print(f'Wrong, try again. Remaining attempts: {attempts}')
```

------------------------------------------------------------------------

# 📝 Notes

These two games were built as part of my **Python learning journey** in
**2025**.\
They focus on practicing: - dictionaries,\
- loops,\
- conditionals,\
- randomness,\
- functions, and\
- user interaction via `input()`/`print()` in **Jupyter Notebook**.

