---
title: "Agentic Search: Decomposing Complex Queries"
slug: agentic-search-decomposing-complex-queries
stage: Build
category: "AI Agent Development"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-search-decomposing-complex-queries
---
# Agentic Search: Decomposing Complex Queries

Get a Python script that turns a complex research query into 3-5 searchable questions using an LLM, with optional search calls for each.

Variables: complex_query

## Prompt

Design an agent that can take a complex user query and decompose it into a series of simpler sub-queries that can be answered by a search tool. This improves the accuracy of research tasks.

**The Problem:**

If a user asks, "What are the pros and cons of using React vs. Vue for a large-scale application?", a single search query might not yield a good answer. The agent needs to be smarter.

**The "Decomposition" Agent:**

1.  **Input:** A complex query `{{complex_query}}`.
2.  **The Prompt:** You will create a prompt for an LLM that asks it to act as a research assistant. The prompt should instruct the LLM to break down the complex query into a list of 3-5 specific, searchable questions.
3.  **Output Format:** The LLM should be instructed to output a JSON list of strings.

**Example:**

*   **Input Query:** "Compare LangChain and LlamaIndex for building RAG systems."
*   **Decomposed Queries (LLM Output):**
    ```json
    [
      "What is LangChain's approach to RAG?",
      "What is LlamaIndex's approach to RAG?",
      "Key differences in data indexing between LangChain and LlamaIndex",
      "Ease of use for building RAG with LangChain vs LlamaIndex"
    ]
    ```

**Your Task:**

Write a Python script that takes a complex query, uses an LLM with your decomposition prompt to generate the sub-queries, and then (optionally) loops through the sub-queries to call a search tool for each.

**Output:**

A Python script that demonstrates the query decomposition process.
