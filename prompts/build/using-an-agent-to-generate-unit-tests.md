---
title: "Using an Agent to Generate Unit Tests"
slug: using-an-agent-to-generate-unit-tests
stage: Build
category: "AI Agent Development"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/using-an-agent-to-generate-unit-tests
---
# Using an Agent to Generate Unit Tests

Build a Python script that uses an LLM to generate and save pytest tests for a function, covering happy paths, edge cases, and errors.

Variables: python_function

## Prompt

Create an AI agent that can write unit tests for a given Python function. This can significantly speed up the development process.

**Agent's Task:**

Given a Python function (`{{python_function}}`), the agent should generate a set of unit tests for it using the `pytest` framework.

The generated tests should cover:
1.  Happy path (expected inputs).
2.  Edge cases (e.g., empty inputs, zeros, boundary values).
3.  Error conditions (if the function is expected to raise exceptions).

**Implementation:**

This is a prompt engineering task.

*   **The Prompt:**
    *   **Role:** "You are a senior software engineer who writes thorough and reliable unit tests."
    *   **Framework:** "You will use the `pytest` framework."
    *   **Task:** "Write a set of unit tests for the following Python function. The tests should cover happy paths, edge cases, and error conditions."
    *   **Input:** Provide the `{{python_function}}`.
    *   **Output Format:** "The output should be a complete, runnable Python script containing the tests."

**Your Task:**

Write a Python script that takes a function, uses an LLM with this prompt to generate the tests, and saves the tests to a file (e.g., `test_my_function.py`).

**Output:**

A Python script that automates the test generation, and the content of the generated test file.
