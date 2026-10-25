---
title: "Advanced RAG: Re-ranking Retrieved Documents"
slug: advanced-rag-re-ranking-retrieved-documents-1
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-re-ranking-retrieved-documents-1
---
# Advanced RAG: Re-ranking Retrieved Documents

Architect a multi-stage RAG pipeline that utilizes cross-encoders to re-rank vector search results for higher response accuracy.

## Prompt

Act as an AI engineer optimizing a Retrieval-Augmented Generation (RAG) system. You've noticed that the initial vector search (the 'retrieval' step) sometimes returns documents that are semantically similar but not truly relevant to the user's query. To fix this, you want to add a 're-ranking' step.

Your task is to design the logic for a RAG pipeline that includes a re-ranking stage using a powerful cross-encoder model.

**Your Task: Design the Pseudocode/Logic**
You are not writing full Python code, but the detailed logic for a function `advanced_rag_query(query: str)`.

**Logic Requirements:**

1.  **Step 1: Initial Retrieval (Bi-Encoder):**
    -   Take the user's `query`.
    -   Generate a single vector embedding for the query using a fast bi-encoder model (like `all-MiniLM-L6-v2` from SentenceTransformers).
    -   Perform a similarity search against your vector database (e.g., ChromaDB) to retrieve the top 10 candidate documents. This is a broad-phase retrieval.

2.  **Step 2: Re-ranking (Cross-Encoder):**
    -   You now have the `query` and a list of 10 candidate documents.
    -   Load a more powerful cross-encoder model (e.g., `'cross-encoder/ms-marco-MiniLM-L-6-v2'`).
    -   A cross-encoder works by taking pairs of (query, document) and outputting a relevance score. You will need to create pairs for your query and each of the 10 documents.
    -   Pass these 10 pairs to the cross-encoder model to get 10 relevance scores.
    -   Sort the candidate documents in descending order based on these new scores.

3.  **Step 3: Augmentation and Generation:**
    -   Select the top 3 documents from the *re-ranked* list.
    -   Construct a prompt for a generator LLM (like GPT-5) that includes the user's `query` and the content of these 3 highly-relevant documents.
    -   Make the final API call to the generator model and return its answer.

**Output Format:**
Provide a well-commented block of pseudocode or a detailed, step-by-step description of the function's logic. Explain *why* a cross-encoder is used for re-ranking (i.e., it's more accurate but slower, so it's used on a small number of candidates).
