---
title: "Building a Simple Recommendation Agent"
slug: building-a-simple-recommendation-agent
stage: Build
category: "AI Agent Development"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-recommendation-agent
---
# Building a Simple Recommendation Agent

Build a Python script that asks for a favorite genre and uses an LLM chain to print movie recommendations with short descriptions.

Variables: genre

## Prompt

Create a very simple recommendation agent that suggests movies to a user based on their stated preferences.

**Agent's Logic:**

1.  The agent asks the user for their favorite movie genre (e.g., "Comedy", "Sci-Fi", "Horror").
2.  The agent then uses an LLM to generate a list of 3-5 recommended movies within that genre.

**Implementation:**

This is a simple conversational chain.

1.  **The Prompt:** Create a prompt template that takes the `{{genre}}` as input.
    *   The prompt should be: "List 5 popular movies in the {{genre}} genre. Provide a one-sentence description for each."
2.  **The Chain:** Create a simple `LLMChain` with this prompt.
3.  **The Interaction:**
    *   First, get the user's favorite genre.
    *   Then, run the chain with that genre as input.
    *   Print the formatted list of recommendations.

**Your Task:**

Write a Python script that implements this simple two-step interaction.

**Output:**

A Python script that asks the user for a genre and then provides movie recommendations.
