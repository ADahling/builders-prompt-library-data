---
title: "Building a Simple Code Style Formatter Agent"
slug: building-a-simple-code-style-formatter-agent
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-code-style-formatter-agent
---
# Building a Simple Code Style Formatter Agent

Get a Python script that asks an LLM to reformat Python snippets to PEP 8 without changing their logic, then prints the formatted code.

Variables: code_snippet

## Prompt

Create a simple AI agent that can reformat a piece of Python code to comply with a specific style guide (e.g., PEP 8).

**Agent's Task:**

Given a piece of poorly formatted Python code (`{{code_snippet}}`), the agent should return the same code but correctly formatted according to PEP 8 standards (e.g., correct indentation, spacing, line length).

**Implementation:**

This is a code generation task.

*   **The Prompt:**
    *   **Role:** "You are an automated Python code formatter."
    *   **Task:** "Reformat the following Python code to be fully compliant with the PEP 8 style guide. Do not change the logic of the code, only its style."
    *   **Input:** Provide the `{{code_snippet}}`.
    *   **Output Format:** "Provide only the formatted code in a single code block."

**Your Task:**

Write a Python script that takes a code snippet, uses an LLM with this prompt to reformat it, and prints the result. Note that using a dedicated tool like `black` or `autopep8` is more reliable in practice, but this demonstrates the agent's capability.

**Output:**

A Python script for the code formatter agent.
