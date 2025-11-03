# Hangman AI Agent with HMM and Reinforcement Learning

## Overview
This project implements an intelligent Hangman solver by combining Hidden Markov Models (HMM) with Reinforcement Learning (RL). The HMM learns letter sequence probabilities from a word corpus, and the RL agent uses those probabilities plus game state information to make smart letter guesses.

## Features
- HMM trained on a corpus of 50,000 words to capture language patterns.
- RL agent trained via Q-Learning or Deep Q-Network to maximize wins and minimize wrong guesses.
- Integration of HMM probabilities to guide exploration and letter selection.
- Evaluation on a hidden test set with scoring based on success rate and guess efficiency.

## Getting Started

### Prerequisites
- Python 3.x
- Packages: numpy, torch, collections

### Usage
1. Load and preprocess the corpus with `load_corpus()`.
2. Train HMM models on corpus for letter transitions.
3. Implement Hangman environment and RL agent.
4. Train the RL agent using HMM probabilities as input features.
5. Evaluate model performance on test words.

## Structure
- `load_corpus.py`: Load and clean training and test word lists.
- `hmm_training.py`: Build and save HMM transition probabilities.
- `hangman_env.py`: Define the game environment and rules.
- `agent.py`: RL agent utilizing HMM information for decision making.
- `train.py`: Training loop combining HMM and RL.
- `evaluate.py`: Test the agent on unseen data and compute metrics.

## Results
The hybrid HMM + RL agent significantly improves performance, reaching higher success rates with fewer wrong guesses compared to baseline frequency-based guessing.

## Acknowledgments
Inspired by classical sequence modeling and reinforcement learning techniques for game AI.

