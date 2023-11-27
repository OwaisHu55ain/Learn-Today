# Python Projects

## 1. Play Guessing Game

```
import random

def play_guessing_game():
    # Generate a random number between 1 and 20 as the secret number
    secret_number = random.randint(1, 20)
    print("I am thinking of a number between 1 and 20")

    # Allow the player to make up to 6 guesses
    for guess_taken in range(1, 7):
        guess = int(input("Please enter your guess here: "))

        if guess < secret_number:
            print("Sorry, your guess is too low. Try again.")
        elif guess > secret_number:
            print("Sorry, your guess is too high. Try again.")
        else:
            # Break out of the loop if the guess is correct
            break

    # Check if the player guessed the correct number
    if guess == secret_number:
        print(f"Congratulations! Your guess {guess} is correct.")
    else:
        print(f"Sorry, the correct number was {secret_number}. Better luck next time.")

 # Call the function to start the guessing game

play_guessing_game()

```

### Summary:

The "play guessing game" function generates a random secret number between 1 and 20, prompting the player to guess the correct number within six attempts. After each guess, the program provides feedback, indicating whether the guess is too high or too low. If the player correctly guesses the secret number, a congratulatory message is displayed; otherwise, the correct number is revealed. The game encourages interactive participation and showcases the use of conditional statements and loops in Python to create a simple yet engaging guessing game.
