---
title: "Building a Simple Recipe Generator Agent"
slug: building-a-simple-recipe-generator-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 83
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-recipe-generator-agent
---
# Building a Simple Recipe Generator Agent

Get a Python script that uses an LLM to turn available ingredients into a formatted recipe with quantities and step-by-step instructions.

Variables: ingredients

## Prompt

Create a simple AI agent that can generate a recipe based on a list of ingredients that the user has.

**Agent's Task:**

Given a list of ingredients (`{{ingredients}}`), the agent should generate a recipe that uses some or all of those ingredients. The recipe should include a title, a list of ingredients (including quantities), and step-by-step instructions.

**Implementation:**

This is a creative generation task for an LLM.

*   **The Prompt:**
    *   **Role:** "You are a creative chef who can come up with delicious recipes using limited ingredients."
    *   **Task:** "Create a recipe using the following ingredients. You can add common pantry staples like salt, pepper, and oil."
    *   **Input:** Provide the list of `{{ingredients}}`.
    *   **Output Format:** "The recipe should have a title, an ingredient list, and instructions."

**Your Task:**

Write a Python script that takes a list of ingredients from the user, uses an LLM with this prompt to generate a recipe, and prints the formatted recipe.

**Output:**

A Python script for the recipe generator.
