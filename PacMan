import random

def choose_word():
    """Function to choose a word randomly from a list."""
    words = ["astronaut", "galaxy", "meteor", "planet", "spaceship", "universe", "comet"]
    return random.choice(words)

def display(word, guesses):
    """Function to display the current state of the game."""
    display_word = ""
    for letter in word:
        if letter in guesses:
            display_word += letter + " "
        else:
            display_word += "_ "
    return display_word.strip()

def play_game():
    word = choose_word()
    guesses = []
    attempts = 6  # or any number you think is appropriate

    print("Welcome to Spaceman!")
    print(f"The secret word has {len(word)} letters.")
    print(display(word, guesses))

    while attempts > 0:
        guess = input("Guess a letter: ").lower()

        if guess in guesses:
            print("You've already guessed that letter.")
        elif guess in word:
            guesses.append(guess)
            print("Correct!")
        else:
            guesses.append(guess)
            attempts -= 1
            print("Wrong! You have " + str(attempts) + " attempts left.")

        print(display(word, guesses))

        if "_" not in display(word, guesses):
            print("Congratulations, you won!")
            return

    print(f"Sorry, you lost! The word was '{word}'.")

if __name__ == "__main__":
    play_game()
