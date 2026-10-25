---
title: "Agentic Error Analysis and Debugging"
slug: agentic-error-analysis-and-debugging
stage: Build
category: "AI Agent Development"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-error-analysis-and-debugging
---
# Agentic Error Analysis and Debugging

Get a Python debugging function that sends code and tracebacks to an LLM for a structured error explanation, root cause, and suggested fix.

Variables: code_snippet, error_traceback

## Prompt

Create an AI agent that helps developers debug their code by analyzing error messages and suggesting fixes.

**Agent's Task:**

Given a snippet of code (`{{code_snippet}}`) and the full error traceback (`{{error_traceback}}`), the agent should:
1.  Explain the error in plain English.
2.  Identify the specific line of code that caused the error.
3.  Suggest a corrected version of the code.

**Implementation:**

This is a prompt engineering task.

*   **The Prompt:**
    *   **Role:** "You are a senior software developer and an expert debugger."
    *   **Context:** Provide the code and the traceback.
    *   **Task:** "Analyze the following error and code. Explain the error, identify the cause, and provide a corrected code snippet."
    *   **Output Format:** Instruct the LLM to provide its answer in a structured Markdown format with clear headings for "Error Explanation", "Root Cause", and "Suggested Fix".

**Your Task:**

Write a Python script that contains a function `debug_code(code, traceback)`. This function should construct the prompt, call the LLM, and print the formatted response.

**Output:**

The Python script and an example of it debugging a simple Python error (e.g., a `TypeError` or `IndexError`).
