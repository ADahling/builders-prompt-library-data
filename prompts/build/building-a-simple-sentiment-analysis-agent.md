---
title: "Building a Simple 'Sentiment Analysis' Agent"
slug: building-a-simple-sentiment-analysis-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 89
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-simple-sentiment-analysis-agent
---
# Building a Simple 'Sentiment Analysis' Agent

Get a Python sentiment classification function using an LLM, with examples that label sentences as Positive, Negative, or Neutral.

Variables: text

## Prompt

Create a basic agent that performs sentiment analysis on a piece of text.

**Agent's Task:**

Given a sentence (`{{text}}`), the agent should classify its sentiment as "Positive", "Negative", or "Neutral".

**Implementation:**

This is a simple classification task, perfect for a single LLM call with a clear prompt.

1.  **The Prompt:**
    *   **Role:** "You are a sentiment analysis model."
    *   **Task:** "Analyze the sentiment of the following text. The sentiment must be one of: Positive, Negative, or Neutral."
    *   **Constraint:** "Your response must be only the single word of the sentiment classification and nothing else."
    *   **Input:** Provide the `{{text}}`.
2.  **The Chain:**
    *   Create a simple `LLMChain` with this prompt.
3.  **Execution:**
    *   Run the chain with a few different sentences (one positive, one negative, one neutral) and print the results.

**Your Task:**

Write a Python script that defines a function `get_sentiment(text)` which uses this prompt to classify the text.

**Output:**

A Python script containing the function and examples of it classifying different sentences.
