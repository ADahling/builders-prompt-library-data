---
title: "Advanced Embeddings: Using Cohere for Multilingual Embeddings"
slug: advanced-embeddings-using-cohere-for-multilingual-embeddings
stage: Build
category: "LLM & AI Integration"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-embeddings-using-cohere-for-multilingual-embeddings
---
# Advanced Embeddings: Using Cohere for Multilingual Embeddings

Implement a Python script using the Cohere API to perform cross-lingual semantic search between Spanish queries and English documents.

## Prompt

You are building a semantic search system for a global e-commerce platform. The product descriptions are in multiple languages (English, Spanish, French). You need an embedding model that can understand the meaning of a query in one language and find relevant documents in another.

Your task is to write a Python script that uses the Cohere Embed API with a multilingual model to demonstrate cross-lingual search.

**Scenario:**
- **Query (in Spanish):** "auriculares inalámbricos con cancelación de ruido"
- **Documents (in English):**
    1. "Wired earbuds with good bass."
    2. "Over-ear Bluetooth headphones with active noise cancellation."
    3. "A guide to writing clean code."

**Goal:** Show that the Spanish query correctly matches the English document about noise-canceling headphones.

**Technical Requirements:**
- Use the 'cohere' and 'numpy' libraries.
- Authenticate using the `COHERE_API_KEY`.
- **Step 1 (Embed):** Make a call to `co.embed()`.
    -   Use a multilingual model, such as `embed-multilingual-v3.0`.
    -   Pass the list of documents and the query in the same API call by specifying the `texts` parameter.
    -   Specify the `input_type` as 'search_document' for the documents and 'search_query' for the query.
- **Step 2 (Separate Embeddings):** The API will return a list of embeddings. Separate the query embedding from the document embeddings.
- **Step 3 (Calculate Similarity):** Use a cosine similarity function (you can write a simple one with NumPy) to calculate the similarity between the Spanish query embedding and each of the English document embeddings.
- **Step 4 (Output):** Print the similarity scores. The score for the second document should be significantly higher than the others, proving the cross-lingual understanding.

**Output Format:**
A complete Python script demonstrating cross-lingual semantic search with Cohere.
