---
title: "Building a Simple ELI5 Agent"
slug: building-a-simple-eli5-explain-like-i-m-5-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 89
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-eli5-explain-like-i-m-5-agent
---
# Building a Simple ELI5 Agent

Get a Python script that uses an LLM to explain complex topics in child-friendly language with simple analogies and prints the explanation.

Variables: complex_topic

## Prompt

Create a simple AI agent that can explain a complex topic in very simple terms, as if explaining it to a 5-year-old.

**Agent's Task:**

Given a `{{complex_topic}}` (e.g., "Quantum Computing", "Blockchain", "General Relativity"), the agent should provide a short, easy-to-understand explanation using simple analogies.

**Implementation:**

This is a prompt engineering task.

*   **The Prompt:**
    *   **Role:** "You are an expert at explaining complex topics to young children."
    *   **Task:** "Explain the following topic to me as if I were 5 years old. Use simple words and analogies."
    *   **Input:** Provide the `{{complex_topic}}`.

**Your Task:**

Write a Python script that takes a complex topic, uses an LLM with this ELI5 prompt to generate the explanation, and prints the result.

**Output:**

A Python script for the ELI5 agent.
