import random

# List of 5 predefined words
words = ["python", "computer", "hangman", "program", "keyboard"]

# Choose a random word
word = random.choice(words)

# Track guessed letters
guessed_letters = []

# Number of incorrect guesses allowed
incorrect_guesses = 0
max_incorrect = 6

print("Welcome to Hangman!")

while incorrect_guesses < max_incorrect:
    # Display the word with unguessed letters hidden
    display_word = ""

    for letter in word:
        if letter in guessed_letters:
            display_word += letter
        else:
            display_word += "_"

    print("\nWord:", " ".join(display_word))
    print("Incorrect guesses:", incorrect_guesses, "/", max_incorrect)

    # Check if the player has won
    if "_" not in display_word:
        print("Congratulations! You guessed the word:", word)
        break

    # Get the player's guess
    guess = input("Guess a letter: ").lower()

    # Check that the guess is a single letter
    if len(guess) != 1 or not guess.isalpha():
        print("Please enter one letter.")
        continue

    # Check if the letter was already guessed
    if guess in guessed_letters:
        print("You already guessed that letter.")
        continue

    guessed_letters.append(guess)

    # Check whether the guess is correct
    if guess in word:
        print("Correct guess!")
    else:
        incorrect_guesses += 1
        print("Incorrect guess!")

else:
    print("\nGame over!")
    print("The word was:", word)
