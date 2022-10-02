# MancalaAI
I try to train an AI to play the game Mancala (Bohnenspiel) using Deep-Q-Learning (in Python). 
If you want to try it out, feel free to download the python notebooks or clone this repo.

**NOTE that the DQN currently does not perform well**

# Explanations of the different notebooks:

## Play.ipynb
Start here if you want to play around a bit. Explains how to:
 - Initialize the Game, Players, Arena
 - Start a game between two Players
 - Train a DQNs by playing the game against another player (Greedy, Random, (Human) or a second competing DQN)
 - Evaluate the performance by playing against other players.

## Classes.ipynb
Defines various classes used in Play.ipynb. The include:
 - Game(): The Mancala Engine. 
 - Memory(): The replay memory used for Deep-Q-Learning
 - Player(): represents the different players
    - RandomPlayer(): Agent that chooses random actions
    - GreedyPlayer(): Greedy agents (chooses those actions with maximal reward)
    - HumanPlayer(): Chooses actions according to input
    - DQNPLayer(): Agent that chooses actions according to predictions of a Deep-Q-Network
  - DQN(): Definition of the Deep-Q-Network
  - Arena: Brings the above objects together to play. Manages the important information and guides it, e.g., to the correct Memory.
  
## Mancala.ipynb
Contains preliminary versions, classes and failed attempts. Does not serve any purpose and can be ignored.

# Sources:
The notebooks use the following packages:
random
numpy
torch
copy

Furthermore, the DQN learning algorithm is heavily inspired and partly copied from a homework of the lecture "Neural Networks & Deep Learning" by Alberto Testolin heard in the winter semester 2020/21 at the university of Padova. 

The game rules (obviously) are those of the game Mancala (Bohnenspiel). There are many different versions of it out there and I simply chose one. 

