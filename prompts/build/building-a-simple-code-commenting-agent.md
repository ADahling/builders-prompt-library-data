---
title: "Building a Simple Code Commenting Agent"
slug: building-a-simple-code-commenting-agent
stage: Build
category: "AI Agent Development"
grade: C
score: 69
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-code-commenting-agent
---
# Building a Simple Code Commenting Agent

Get a Python script that uses an LLM to add inline comments without changing code, plus a before-and-after example for explaining function logic.

Variables: python_function

## Prompt

Create a simple AI agent that can add comments to a given piece of Python code to explain what it does.

**Agent's Task:**

Given a Python function (`{{python_function}}`) that has no comments, the agent should return the same function but with inline comments added to explain complex lines or blocks of code.

**Implementation:**

This is a code generation task.

*   **The Prompt:**
    *   **Role:** "You are a helpful programming assistant who writes clear and concise code comments."
    *   **Task:** "Add inline comments to the following Python function to explain its logic. Do not change the code itself, only add comments."
    *   **Input:** Provide the `{{python_function}}`.

**Your Task:**

Write a Python script that takes a Python function as a string, uses an LLM with this prompt to add comments, and then prints the commented code.

**Output:**

A Python script and an example of a function before and after the agent has added comments.
