---
title: "Building a Code Documentation Agent"
slug: building-a-code-documentation-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-code-documentation-agent
---
# Building a Code Documentation Agent

Get a Python script that calls an LLM to generate Google Style docstrings for Python code, with a sample function demonstration.

Variables: code_snippet

## Prompt

Create an AI agent that automatically generates documentation for a given Python function or class. The agent should analyze the code and produce a well-formatted docstring.

**Agent's Task:**

Given a piece of Python code (`{{code_snippet}}`), the agent should generate a docstring in a standard format (like Google Style or reStructuredText).

The docstring should include:
1.  A brief summary of the function/class's purpose.
2.  Descriptions of all arguments (`Args:`).
3.  A description of the return value (`Returns:`).
4.  Any exceptions that might be raised (`Raises:`).

**Implementation:**

This is a prompt engineering task that can be solved with a single, well-structured LLM call.

*   **The Prompt:**
    *   **Role:** "You are an expert Python programmer who writes clear and comprehensive documentation."
    *   **Task:** "Generate a Google Style docstring for the following Python code."
    *   **Input:** Provide the `{{code_snippet}}`.
    *   **Constraint:** "The docstring should be complete and ready to be inserted directly into the code."

**Your Task:**

Write a Python function that takes a code snippet, constructs this prompt, calls an LLM, and returns the generated docstring.

**Output:**

A Python script containing the function and an example of it generating a docstring for a sample function.
