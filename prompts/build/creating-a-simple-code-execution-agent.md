---
title: "Creating a Simple Code Execution Agent"
slug: creating-a-simple-code-execution-agent
stage: Build
category: "AI Agent Development"
grade: B
score: 72
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-simple-code-execution-agent
---
# Creating a Simple Code Execution Agent

Get a Python script that answers questions by generating and executing LLM-written code, capturing its output, and noting security risks.

## Prompt

Build a very basic agent that can write and execute Python code to answer a question. This is a foundational pattern for more advanced coding agents.

**WARNING:** Executing LLM-generated code is inherently risky. This should be done in a sandboxed environment.

**The Workflow:**

1.  **The Prompt:** The user asks a question that is best solved with code, e.g., "What are the first 10 prime numbers?"
2.  **Code Generation:** Use an LLM with a prompt that asks it to write a Python script to answer the question. The prompt should instruct the LLM to only output the raw Python code and nothing else.
3.  **Code Execution:**
    *   Take the generated Python code.
    *   Use Python's `exec()` function to execute it. You must capture the output (e.g., by redirecting `stdout`).
4.  **Final Answer:** The captured output from the script is the final answer.

**Your Task:**

Write a Python script that orchestrates this simple workflow. It should take a user's question, call the LLM to generate code, execute the code, and print the result.

**Output:**

A Python script that demonstrates this code generation and execution loop. Include comments about the security risks.
