# Rock Paper Scissors Game

## Overview
This is a simple command-line game of Rock, Paper, Scissors created in Python. The player selects either Rock, Paper, or Scissors, and the computer makes a random choice. The winner is determined based on the standard rules of Rock, Paper, Scissors:

- Rock crushes Scissors
- Scissors cut Paper
- Paper covers Rock

## How to Play
1. Run the game in a Python environment.
2. When prompted, enter one of the following options:
   - **r** for Rock
   - **p** for Paper
   - **s** for Scissors
3. The computer will make its choice, and the game will display the result (win, lose, or draw).

## Rules
- **Rock** beats **Scissors**
- **Scissors** beat **Paper**
- **Paper** beats **Rock**

If both the player and computer choose the same option, it’s a draw.

## Code Explanation

### Key Components
- **Player Move**: The player is prompted to choose Rock, Paper, or Scissors.
- **Computer Move**: The computer randomly selects Rock, Paper, or Scissors using the `random.randint` function.
- **Outcome Calculation**: The game compares the player’s choice and the computer’s choice to determine the result.

### Code Example
Here’s a quick look at the main parts of the code:

```python
import random

rock = 'Rock'
paper = 'Paper'
scissors = 'Scissors'
player_move = input('Choose [r]ock, [p]aper or [s]cissors: ')

# Mapping player input to the corresponding move
if player_move == 'r':
    player_move = rock
elif player_move == 'p':
    player_move = paper
elif player_move == 's':
    player_move = scissors
else:
    raise SystemExit('Invalid input. Try again...')

# Randomly generating the computer's move
computer_random_number = random.randint(1, 3)
if computer_random_number == 1:
    computer_move = rock
elif computer_random_number == 2:
    computer_move = paper
else:
    computer_move = scissors

# Determining the outcome
if (player_move == rock and computer_move == scissors) or \
   (player_move == paper and computer_move == rock) or \
   (player_move == scissors and computer_move == paper):
    print('You win!')
elif player_move == computer_move:
    print('Draw!')
else:
    print('You lose!')
