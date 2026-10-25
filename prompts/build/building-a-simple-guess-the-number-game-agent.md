---
title: "Building a Simple 'Guess the Number' Game Agent"
slug: building-a-simple-guess-the-number-game-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 82
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-guess-the-number-game-agent
---
# Building a Simple 'Guess the Number' Game Agent

Build a command-line Python number guessing game with high and low hints, a secret number from 1 to 100, and a guess counter.

## Prompt

Create an AI agent that plays a "guess the number" game with the user. The agent will think of a number, and the user will try to guess it.

**Agent's Logic:**

1.  **Setup:** The agent secretly chooses a random number between 1 and 100.
2.  **State:** The agent needs to remember the secret number and the number of guesses the user has made.
3.  **The Loop:**
    *   The agent asks the user for their guess.
    *   The agent compares the guess to the secret number.
    *   It responds with "Too high," "Too low," or "Correct!"
    *   The loop continues until the user guesses correctly.
4.  **Conclusion:** When the user wins, the agent tells them how many guesses it took.

**Implementation:**

This can be implemented with a simple Python class to manage the game state and a `while` loop for the interaction. The agent's responses ("Too high," etc.) are determined by simple `if` statements, not an LLM. An LLM can be used to make the agent's personality more engaging, but it's not required for the core game logic.

**Your Task:**

Write a Python script that implements this game. The script should be playable from the command line.

**Output:**

A complete, runnable Python script for the number guessing game.
