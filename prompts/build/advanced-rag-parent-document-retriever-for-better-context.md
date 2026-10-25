---
title: "Advanced RAG: Parent Document Retriever for Better Context"
slug: advanced-rag-parent-document-retriever-for-better-context
stage: Build
category: "LLM & AI Integration"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-parent-document-retriever-for-better-context
---
# Advanced RAG: Parent Document Retriever for Better Context

Implement a two-stage retrieval strategy that uses child-chunk vector search to fetch context-rich parent documents for higher RAG accuracy.

## Prompt

Act as an AI engineer improving a RAG system that works with long documents (e.g., research papers, legal contracts). A common problem is that the best-matching text chunk from a vector search is too small and lacks the surrounding context. You will implement the 'Parent Document Retriever' strategy to solve this.

**Your Task: Design the Pseudocode/Logic**
Design the logic for setting up and querying a Parent Document Retriever.

**Logic Requirements:**

**Part 1: The Indexing Pipeline**
1.  **Load Documents:** Start with a list of long documents.
2.  **Create Child Chunks:** For each document, use a `RecursiveCharacterTextSplitter` to split it into small, manageable chunks (e.g., 400 characters). These are the 'child' chunks.
3.  **Create Parent Chunks:** For each document, also create larger chunks (e.g., 2000 characters) that overlap. These are the 'parent' chunks.
4.  **Store in Two Places:**
    -   **Vector Store:** Generate embeddings for the *small child chunks only*. Store these embeddings and the text of the child chunks in your vector database (e.g., ChromaDB).
    -   **Document Store:** Create a simple key-value store (like a Python dictionary) where you store the *large parent chunks*. Each parent chunk should have a unique ID.
5.  **Link Child to Parent:** When you store a child chunk in the vector store, you must add metadata that includes the ID of the parent chunk it belongs to.

**Part 2: The Retrieval Pipeline**
1.  **Query:** A user submits a query.
2.  **Search Child Chunks:** Perform a similarity search against the vector store using the query. This will retrieve the most relevant *small child chunks*.
3.  **Find the Parents:** For each retrieved child chunk, look at its metadata to find the ID of its parent chunk.
4.  **Retrieve Parent Chunks:** Use the parent IDs to look up the corresponding *large parent chunks* from your document store.
5.  **Augment and Generate:** Pass these large, context-rich parent chunks to your LLM to generate the final answer.

**Output Format:**
Provide a detailed, step-by-step description of this two-part process. Explain why this method is effective (it combines the precise search of small chunks with the rich context of large chunks).
