---
title: "Advanced RAG: The RAPTOR Strategy for Multi-level Summarization"
slug: advanced-rag-the-raptor-strategy-for-multi-level-summarization
stage: Build
category: "LLM & AI Integration"
grade: B
score: 72
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-the-raptor-strategy-for-multi-level-summarization
---
# Advanced RAG: The RAPTOR Strategy for Multi-level Summarization

Implement the RAPTOR strategy to build a hierarchical summary tree for multi-level document retrieval and complex query processing.

## Prompt

Act as an AI researcher implementing the RAPTOR (Recursive Abstractive Processing for Tree-Organized Retrieval) strategy. This advanced RAG technique builds a hierarchical summary tree over your documents, allowing for retrieval across different levels of abstraction.

**Your Task: Design the Pseudocode/Logic for the RAPTOR Indexing Process**

**Logic Requirements:**

**Part 1: The Indexing Tree**

1.  **Level 0 (Initial Chunks):**
    -   Start with a collection of raw documents.
    -   Split these documents into small, contiguous text chunks. These are the leaves of your tree (Level 0).

2.  **Clustering Level 0:**
    -   Generate embeddings for all Level 0 chunks.
    -   Use a clustering algorithm (e.g., UMAP + HDBSCAN) to group these chunks into semantic clusters.

3.  **Level 1 (Summarizing Clusters):**
    -   For each cluster of chunks from the previous step:
        -   Concatenate the text of all chunks within that cluster.
        -   Use a powerful LLM (e.g., GPT-5) with a prompt like: "Summarize the following text, which is a collection of related document chunks, into a single, coherent paragraph."
    -   The resulting summaries are your Level 1 nodes.

4.  **Recursive Clustering and Summarization (Levels 2, 3, ...):**
    -   Now, treat the Level 1 summaries as your new set of documents.
    -   Recursively repeat the process: generate embeddings for the Level 1 summaries, cluster them, and use an LLM to summarize each new cluster to create Level 2 nodes.
    -   Continue this process until you have a small number of nodes at the top level (e.g., less than 10), forming the apex of your summary tree.

**Part 2: The Retrieval Process**
1.  **Multi-level Search:** When a user queries, you search across *all* nodes at *all* levels of the tree simultaneously.
2.  **Return Context:** The retrieved nodes (which could be detailed leaf chunks or high-level summaries) are then passed to the generator LLM.

**Output Format:**
Provide a detailed, step-by-step description of the RAPTOR indexing and retrieval process. Explain why this hierarchical approach can answer both very specific and very broad questions effectively.
