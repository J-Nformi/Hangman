# Hangman
Hangman is a simple yet entertaining game where players guess letters within a limited number of attempts to reveal a hidden word. 

The code implements the Hangman game in Python, pulling a word from an online word list and allowing the player to guess letters to reveal the hidden word. Here's a step-by-step explanation for the code:

**Game Initialization**

The code fetches a list of words from an online source and filters them to create text_list containing only alphabetical words in uppercase.
It defines a dictionary hangman representing the stages of the hangman drawing.

**Game Setup**

The user chooses a game level: Easy (2 hints with 2 mistakes left), Medium (1 hint with 2 mistakes left), or Hard (No hints).
A random word is chosen from text_list, and a hidden_word variable is initialized to display dashes corresponding to the letters in the chosen word.

**Gameplay**

The player has a limited number of attempts represented by mistake_count (initialized as 6).
They can input a letter as a guess. The code checks if the input is a valid single alphabet and whether it has been guessed before.
If the guessed letter is correct, it reveals the letter in the hidden_word, updating its display.
If the guessed letter is incorrect, it decrements mistake_count and shows a part of the hangman corresponding to the number of mistakes.
There's a helper function help_function to give hints based on the game level chosen.

**Game Execution**

Depending on the chosen level, the game progresses:
In Hard mode (level 3), the player plays without hints until they either win or exhaust their attempts.
In Medium and Easy modes (levels 2 and 1), hints are provided based on the rules defined.

**Game Outcome**

If the player exhausts all attempts (mistake_count == 0), they lose and the hanged message is displayed, along with the actual word.
If the player successfully guesses the word (hidden_word.count('-') == 0), they win, and a congratulations message is shown.
The code structure includes functions for gameplay, level selection, hints, and game execution loops, making it interactive and flexible based on the chosen difficulty level.
