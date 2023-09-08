# Maze Navigation using Q-Learning

## Introduction

This project, developed by Niloufar Baba Ahmadi (Student ID: 610398103), implements a Q-Learning algorithm to solve a maze navigation problem. The objective is to train an agent to navigate a 2D maze, reaching the goal state while avoiding obstacles and collecting flags along the way. This implementation uses the Q-Learning algorithm to update the Q-table, which stores estimated rewards for different actions in each state.

## Dependencies

Make sure you have the following Python libraries installed:

- `numpy`
- `networkx`
- `matplotlib`

## Overview

The agent can take four possible actions in the maze: "up," "down," "left," or "right."

```python
actions = ["up", "down", "left", "right"]
```

The code provides functions for calculating the next state and reward, choosing an action based on the Q-table, and applying the Q-Learning algorithm.

## Training Environment

The maze is represented as a grid, where each cell has a specific value:

- `0`: Free to move
- `2`: Blocks (obstacles)
- `1`: Goal state
- Flag state is one of the free-to-move states also present in the flag set.

The starting state is `(0, 0)`, and flags are located at `(0, 1)`.

```python
maze = [
    [0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0],
    [0, 2, 0, 0, 0],
    [0, 0, 0, 0, 1]
]
```

## Q-Learning Parameters

- `alpha`: Learning rate (0.9)
- `gamma`: Discount factor (1)
- `epsilon`: Exploration rate (0.4)
- Maximum number of episodes: 50

## Additional Information

- The Q-table stores estimated rewards for taking different actions in each state.
- The get_path function generates the best path using the Q-table.
- The assignment answers questions regarding the number of states and the impact of different alpha and gamma values on the Q-Learning process.
- An illustration of the Q-table as a weighted graph is provided using NetworkX and Matplotlib.
