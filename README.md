<p align="center"><img src="https://github.com/nathanbronson/Pokerisk/blob/main/logo.jpg?raw=true" alt="logo" width="200"/></p>

_____
# Pokerisk
poker bet-sizing optimized by self-play and gradient descent

## About
*Pokerisk is a work-in-progress, and more simulations will be implemented to better approximate the game of poker and improve the simulation-loss-function-complex's convexity and differentiability.*

Pokerisk is poker bet-sizing algorithm optimized by self-play in a simplified bidding environment resembling a game of poker. Pokerisk represents a bet-sizing policy as a three-dimensional array, and indexes it conditionally to determine how much it will bet. The dimensions represent the probability of winning a hand given the agent's hand, the largest bet in the round so far as a proportion of that bettor's stack, and the total pot size as a proportion of all available currency.

In each batch, agents play thousands of hands using the current optimal strategy with some added noise. Each agent's performance is scored based on their profit or loss, and these values are aggregated and back propogated to the strategy parameters. Pokerisk has an unfortunate affinity for local minima.

## Usage
Simulations are implemented in the notebook, `pokerisk.ipynb`. They can be executed for a given number of iterations, and the optimized strategy can then be saved. Several simulations are implemented, including a basic simulation, a noised simulation, and a more complicated simulation implementing basic calling.

## License
See `LICENSE`.