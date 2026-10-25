---
title: "Introduction to Semantic Routing"
slug: introduction-to-semantic-routing
stage: Build
category: "AI Agent Development"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/introduction-to-semantic-routing
---
# Introduction to Semantic Routing

Get an explanation and Python script for routing user queries by meaning, using predefined routes, embeddings, and cosine similarity.

Variables: user_query

## Prompt

Explain the concept of Semantic Routing and demonstrate how to implement a simple version of it. Semantic routing is a technique used to direct user queries to different agents or prompt chains based on the *meaning* of the query, rather than keyword matching.

**Concept:**

Instead of using an LLM to decide where to route a query (which is slow and expensive), semantic routing uses embeddings. You embed the user's query and compare it to the embeddings of predefined "routes" or "intents".

**Implementation Steps:**

1.  **Define Routes:** Create a few categories, e.g., "Billing", "Technical Support", "General Inquiry".
2.  **Create Utterances:** For each route, provide a list of example phrases.
    *   Billing: ["I want to cancel my subscription", "Where is my invoice?"]
    *   Tech Support: ["The app is crashing", "How do I reset my password?"]
3.  **Embeddings:** Use an embedding model (like OpenAI's `text-embedding-ada-002`) to generate vector embeddings for all the example utterances.
4.  **The Router Function:**
    *   Take a new `{{user_query}}`.
    *   Embed the query.
    *   Calculate the cosine similarity between the query embedding and all the utterance embeddings.
    *   Find the utterance with the highest similarity score.
    *   Return the route associated with that utterance.

**Output:**

A Python script that implements this logic. It should define the routes, embed them, and then test a few new queries to show that they are routed correctly based on semantic similarity.
