---
title: "Cost Optimization: Using a Cascade of Models"
slug: cost-optimization-using-a-cascade-of-models
stage: Build
category: "LLM & AI Integration"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/cost-optimization-using-a-cascade-of-models
---
# Cost Optimization: Using a Cascade of Models

Architect a cost-efficient model router that uses small models to classify and handle simple queries while escalating complex tasks to LLMs.

## Prompt

Act as a senior AI architect designing a cost-effective solution for a multi-purpose chatbot. Some user queries are simple (e.g., "What's your name?"), while others are complex (e.g., "Write a detailed business plan..."). Using a powerful, expensive model like GPT-5 for every query is wasteful.

Your task is to design the logic for a 'model cascade' or 'router'. This system will first use a cheap, fast model to classify the user's query. If the query is simple, the cheap model will answer it. If it's complex, the system will then route the query to a more powerful, expensive model.

**Your Task: Design the Pseudocode/Logic**
You are not writing full Python code, but the detailed logic or pseudocode for a function called `handle_query(query_text)`.

**Logic Requirements:**
1.  **First Pass (Classification):**
    -   Make an API call to a cheap, fast model (e.g., Claude Sonnet 5 or GPT-5).
    -   The prompt to this model should be a classification prompt. It should ask the model to classify the `query_text` into one of two categories: "simple" or "complex".
    -   The prompt must give clear definitions: a "simple" query can be answered with common knowledge and a short response. A "complex" query requires deep reasoning, creativity, or extensive knowledge.
    -   Instruct the model to respond with only the word "simple" or "complex".

2.  **Conditional Routing:**
    -   If the classification response is "simple":
        -   Make a second API call to the *same cheap model*.
        -   This time, the prompt is the original `query_text`
