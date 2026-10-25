---
title: "Advanced RAG: Parent Document Retriever"
slug: advanced-rag-parent-document-retriever
stage: Build
category: "AI Agent Development"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-parent-document-retriever
---
# Advanced RAG: Parent Document Retriever

Implement an advanced Retrieval-Augmented Generation RAG strategy using the "Parent Document Retriever".

## Prompt

Implement an advanced Retrieval-Augmented Generation (RAG) strategy using the "Parent Document Retriever". This technique improves performance by retrieving smaller chunks for better search accuracy, but passing larger, more context-rich chunks to the LLM.

**The Problem:**

Small chunks are good for semantic search, but they often lack the surrounding context that the LLM needs to generate a good answer. Large chunks have context but are bad for search.

**The Solution (Parent Document Retriever):**

1.  **Splitting:** You split your documents in two ways:
    *   Small "child" chunks that will be embedded.
    *   Large "parent" chunks that contain the full context.
2.  **Storage:** You need a way to link the child chunks to their parent chunks.
    *   The `InMemoryStore` can be used to hold the parent documents.
    *   A vector store (like Chroma) holds the child chunk embeddings.
3.  **Retrieval:**
    *   The `ParentDocumentRetriever` first performs a search over the small child chunks in the vector store.
    *   Once it finds the relevant child chunks, it uses the link to retrieve their corresponding large parent chunks from the document store.
4.  **Generation:** These larger, more context-rich parent chunks are then passed to the LLM.

**Your Task:**

Write a Python script using LangChain to implement a RAG pipeline with the `ParentDocumentRetriever`.

**Output:**

A Python script that sets up the dual-chunking, the stores, and the retriever, and then answers a question using this advanced RAG method.
