---
title: "Building a Simple Regex Generation Agent"
slug: building-a-simple-regex-generation-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-regex-generation-agent
---
# Building a Simple Regex Generation Agent

Get a Python script that takes a plain-language pattern description, asks an LLM for a matching regex, and prints the expression.

Variables: pattern_description

## Prompt

Create a simple AI agent that can generate a regular expression (regex) from a natural language description.

**Agent's Task:**

Given a description of a pattern (`{{pattern_description}}`), the agent should generate the corresponding regex.

**Implementation:**

This is a prompt engineering task.

*   **The Prompt:**
    *   **Role:** "You are an expert in regular expressions."
    *   **Task:** "Write a regex that matches the following pattern. Provide only the regex itself."
    *   **Input:** Provide the `{{pattern_description}}`.

**Example:**

*   **Description:** "A valid email address."
*   **Expected Output:** `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$`

**Your Task:**

Write a Python script that takes a pattern description, uses an LLM with this prompt to generate the regex, and prints the result.

**Output:**

A Python script for the regex generation agent.
