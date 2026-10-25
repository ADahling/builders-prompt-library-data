---
title: "Advanced RAG: Query Transformations"
slug: advanced-rag-query-transformations
stage: Build
category: "AI Agent Development"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-query-transformations
---
# Advanced RAG: Query Transformations

Get a Python RAG script that rewrites user queries with an LLM before vector retrieval and displays the original and rewritten queries.

Variables: query

## Prompt

Improve a RAG system by implementing query transformations. Instead of using the user's raw query for retrieval, you transform it to be more effective for a vector search.

**The Problem:**

User queries are often short, conversational, or use different vocabulary than the documents in the knowledge base. This can lead to poor retrieval results.

**The Solution: Query Transformations**

Before the retrieval step, pass the user's query through an LLM to transform it. Here are a few transformation techniques:

1.  **Rewrite:** Rephrase the query to be more explicit and detailed. (e.g., "agent memory" -> "How is memory implemented in AI agents for long-term context?").
2.  **Hypothetical Document (HyDE):** Generate a hypothetical answer and use its embedding (as seen in another prompt).
3.  **Sub-Questions:** Decompose the query into several sub-questions and retrieve documents for each.

**Your Task:**

Implement the **Rewrite** technique.

1.  Create a prompt that instructs an LLM to take a user's `{{query}}` and rewrite it to be an ideal query for a vector database search.
2.  In your RAG pipeline, add this step before the retriever is called.
3.  Use the embedding of the *rewritten query* to perform the retrieval.

**Output:**

A Python script that demonstrates this query-rewriting RAG pipeline. The output should show the original query and the LLM-generated rewritten query.
