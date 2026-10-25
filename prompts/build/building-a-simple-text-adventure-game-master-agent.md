---
title: "Building a Simple 'Text Adventure' Game Master Agent"
slug: building-a-simple-text-adventure-game-master-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-text-adventure-game-master-agent
---
# Building a Simple 'Text Adventure' Game Master Agent

Create an AI agent that acts as a Game Master GM for a simple text adventure game.

## Prompt

Create an AI agent that acts as a Game Master (GM) for a simple text adventure game.

**The Game:**

The user is a character in a story. The agent describes the scene, and the user types what they want to do. The agent then describes the result of that action.

**Implementation:**

This is a conversational agent with memory and a carefully crafted system prompt.

*   **The Prompt:**
    *   **Role:** "You are the Game Master for a fantasy text adventure game. Your goal is to create a fun and engaging story."
    *   **Rules:**
        *   "Start by describing the opening scene: 'You are in a dark forest. There is a path to the north and a cave to the east.'"
        *   "Wait for the user to tell you what they want to do."
        *   "Describe the outcome of their action in a creative way."
        *   "Always end your response by describing the new scene and presenting the user with 2-3 choices of what to do next."
*   **Memory:** Use `ConversationBufferMemory` to keep track of the story so far.

**Your Task:**

Write a Python script that sets up a `ConversationChain` with this GM prompt and memory. The script should have a loop to allow the user to play the game.

**Output:**

A Python script for the text adventure game and a sample of the first few turns of a game.
