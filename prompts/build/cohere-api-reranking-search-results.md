---
title: "Cohere API: Reranking Search Results"
slug: cohere-api-reranking-search-results
stage: Build
category: "LLM & AI Integration"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cohere-api-reranking-search-results
---
# Cohere API: Reranking Search Results

Create a Python script using the Cohere Rerank API to semantically reorder e-commerce search results for improved query relevance.

## Prompt

You are improving the search functionality of an e-commerce website. The current keyword-based search returns many results, but the most relevant ones aren't always at the top. You decide to use the Cohere Rerank API to reorder the results based on semantic relevance to the user's query.

Your task is to write a Python script that uses the Cohere API to rerank a list of product descriptions.

**Scenario:**
- **Query:** "wireless noise-canceling headphones for travel"
- **Documents (Initial Search Results):**
    1. "Wired earbuds with good bass."
    2. "Over-ear Bluetooth headphones with active noise cancellation and 30-hour battery life."
    3. "A travel guide to Europe."
    4. "Noise-canceling earplugs for sleeping."
    5. "Compact wireless earbuds, great for the gym."

**Technical Requirements:**
- Use the 'cohere' Python SDK.
- Authenticate using the `COHERE_API_KEY` environment variable.
- Call the `co.rerank()` method.
- Pass the query and the list of documents.
- Use the `rerank-english-v3.0` model.
- Request the top 3 results (`top_n=3`).
- The script should iterate through the reranked results and print the document text and its new relevance score, showing that document #2 is now ranked highest.

**Output Format:**
A complete Python script demonstrating the Cohere Rerank API.
