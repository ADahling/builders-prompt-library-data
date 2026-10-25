---
title: "Advanced RAG: HyDE (Hypothetical Document Embeddings)"
slug: advanced-rag-hyde-hypothetical-document-embeddings
stage: Build
category: "AI Agent Development"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-hyde-hypothetical-document-embeddings
---
# Advanced RAG: HyDE (Hypothetical Document Embeddings)

Implement the HyDE Hypothetical Document Embeddings technique to improve the performance of a RAG system.

Variables: question

## Prompt

Implement the HyDE (Hypothetical Document Embeddings) technique to improve the performance of a RAG system. HyDE works by first generating a hypothetical answer to the user's question and then using the embedding of that *answer* to perform the retrieval, which is often more effective than using the embedding of the question itself.

**The Workflow:**

1.  **User Question:** The user asks a question, e.g., "What is the ReAct framework for AI agents?"
2.  **Hypothetical Document Generation:**
    *   Use an LLM with a specific prompt: "Please write a short, hypothetical document that answers the following question: '{{question}}'".
    *   The LLM will generate a plausible-sounding answer, even if it's not factually perfect.
3.  **Embedding:**
    *   Generate an embedding for this *hypothetical document*.
4.  **Retrieval:**
    *   Use this embedding to search your vector store for the most similar *real* documents.
5.  **Final Generation:**
    *   Pass the user's original question and the retrieved real documents to the final LLM to generate the answer.

**Your Task:**

Write a Python script that implements this HyDE workflow. You will need two LLM calls: one to generate the hypothetical document and one to generate the final answer.

**Output:**

A Python script that demonstrates the HyDE process, showing the generated hypothetical document and the final answer.
