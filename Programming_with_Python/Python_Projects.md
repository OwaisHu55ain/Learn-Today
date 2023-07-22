# Python Projects

## 1. Guess The Number

```
 # This is the guess number game.

import random

secretNumber = random.randint(1,20)
print('I am thinking of number between 1 and 20.')
 # Ask the playes to guess 6 times.

for guessTaken in range (1,7):
    print('Take a guess between 1 to 20.')
    guess = int(input('Enter number here: '))
    
    if guess < secretNumber:
        print('Sorry, Guess again. Your guess is to low.')
    elif guess > secretNumber:
        print('Sorry, Guess Again. Your guess is to high.')
    else:
        break # This condition is correct guess.

if guess == secretNumber:
    print(f'Great Job! You guessed my number {secretNumber} correctly.')
else:
    print(f'Nope. The number I was thinking of {secretNumber}, Better luck next time.')

```
## 2. Tic Tac Toe Game

```
board = {1:'  ',2:'  ', 3:'  ', 4:'  ',5:'  ', 6:'  ', 7:'  ', 8:'  ', 9:'  ',}
    

def theBoard(board):
    print(board[1]+'|'+board[2]+'|'+board[3])
    print('--+--+--')
    print(board[4]+'|'+board[5]+'|'+board[6])
    print('--+--+--')
    print(board[7]+'|'+board[8]+'|'+board[9])
    
turn = 'X'

for game in range(len(board)):
    theBoard(board)
    move = int(input('Please enter your move here: '))
    board[move] = turn
    if turn == 'X':
        turn = 'O'
    else:
        turn = 'X'
    

theBoard(board)
```
## 3. Guess The Number (Computer)

```
import random

def computer_guess(x):
    low = 1
    high = x
    feedback = ''
    while feedback != 'c': 
        if low != high:
            guess = random.randint(low, high)
        else:
            guess = low
        feedback = input(f'Is this {guess} number? Plesse share your feedback, Is it High (H), Low (L) or Correct (C):' ).lower()
        if feedback == 'h':
            high = guess-1
        elif feedback == 'l':
            low = guess+1
    
    print(f'Horray! Computer guessed your number {guess}, Correctly..')

computer_guess(100)

```
