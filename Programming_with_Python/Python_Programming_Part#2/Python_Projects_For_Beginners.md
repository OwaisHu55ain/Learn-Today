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


## 2. Tic Tac Toe

```
 # Define an empty tic-tac-toe board using a dictionary
tic_tac_toe_board = {1: " ", 2: " ", 3: " ", 4: " ", 5: " ", 6: " ", 7: " ", 8: " ", 9: " "}

def display_board(board):
    # Display the current state of the tic-tac-toe board
    print(board[1] + "|" + board[2] + "|" + board[3])
    print("-+-+-")
    print(board[4] + "|" + board[5] + "|" + board[6])
    print("-+-+-")
    print(board[7] + "|" + board[8] + "|" + board[9])

current_turn = "X"

 # Allow each player to make a move alternately until the board is filled
for move in range(len(tic_tac_toe_board)):
    display_board(tic_tac_toe_board)
    player_move = int(input("Player " + current_turn + ", enter your move (1-9): "))
    
    # Update the board with the player's move
    tic_tac_toe_board[player_move] = current_turn
    
    # Switch turns between "X" and "O"
    current_turn = "O" if current_turn == "X" else "X"

 # Display the final state of the tic-tac-toe board
display_board(tic_tac_toe_board)

```

### Summary:

In above code defines a basic tic-tac-toe game where players "X" and "O" take turns making moves on a 3x3 grid represented by a dictionary. The display_board function shows the current state of the board, and the game alternates between players until the board is filled. Players input their moves, updating the board accordingly, and the program switches turns. The final state of the board is displayed, reflecting the moves made by both players throughout the game. The code showcases the use of a dictionary to represent the game board, alternating turns between players, and dynamically updating the board based on user input, creating a simple interactive tic-tac-toe experience.


## Number Guessing Game (Computer)



```python
import random

def computer_guess(x):
    # Set the initial range for the computer's guess
    low = 1
    high = x
    
    # Initialize feedback variable to a value that won't trigger the loop initially
    feedback = ''
    
    # Continue looping until the feedback is 'c' (correct)
    while feedback != 'c': 
        # Check if the range is not a single number
        if low != high:
            # Generate a random guess within the current range
            guess = random.randint(low, high)
        else:
            # If the range is a single number, set the guess to that number
            guess = low
        
        # Get feedback from the user about the computer's guess
        feedback = input(f'Is this {guess} number? Please share your feedback, Is it High (H), Low (L) or Correct (C):' ).lower()
        
        # Adjust the range based on the user's feedback
        if feedback == 'h':
            high = guess - 1
        elif feedback == 'l':
            low = guess + 1
    
    # Print a message when the correct number is guessed
    print(f'Hooray! Computer guessed your number {guess} correctly.')

 # Call the function with an example range (e.g., 1 to 100)
computer_guess(100)
```
### Summary
This code represents a simple number guessing game where the computer tries to guess a number that the user has in mind. The user provides feedback ('H' for too high, 'L' for too low, 'C' for correct), and the computer adjusts its guess accordingly until it correctly guesses the user's number.
