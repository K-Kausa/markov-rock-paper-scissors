# markov-rock-paper-scissors
A Rock-Paper-Scissors bot that learns and predicts opponent moves using a Markov Chain

## About the Project

This project simulates a match of n rounds between two bots:
* **Player 1:** Plays based on a static (random generated), hidden transition matrix (Markov Chain). Its current move depends heavily on its previous move.
* **Player 2 (The Learning Bot):** Starts with the same propability for each move but builds an observation matrix in real-time. It predicts Player 1's next move based on his previous moves.

## ⚙️ How It Works

1. **State Tracking:** Player 2 tracks the frequency of Player 1's moves following any given move (e.g., "How often does Player 1 play Rock after playing Scissors?").
2. **Probability Matching:** Instead of playing randomly, Player 2 weighs its choices based on the observed data, favoring the exact counter to Player 1's most likely next move.

## 📊 Mathematical Curiosity: Ties vs. Player 1 Wins

An interesting property of this specific probability-matching algorithm is that Player 1's win rate will always converge with the tie rate. 
