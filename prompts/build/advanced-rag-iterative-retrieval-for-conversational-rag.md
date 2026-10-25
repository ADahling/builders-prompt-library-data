---
title: "Advanced RAG: Iterative Retrieval for Conversational RAG"
slug: advanced-rag-iterative-retrieval-for-conversational-rag
stage: Build
category: "LLM & AI Integration"
grade: B
score: 77
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-iterative-retrieval-for-conversational-rag
---
# Advanced RAG: Iterative Retrieval for Conversational RAG

Engineer a multi-step RAG pipeline that rewrites contextual follow-up questions into standalone queries to ensure accurate vector search.

## Prompt

You are building a conversational RAG chatbot. A user might ask a follow-up question that only makes sense in the context of the conversation. A standard RAG system would fail because the follow-up question itself (e.g., "Why?") is not semantically meaningful on its own.

**Your Task:** Design the logic for an 'iterative retrieval' pipeline that handles conversational context.

**Scenario:**
- **Conversation History:**
    1.  **User:** "What is the RAG technique?"
    2.  **Bot:** (After retrieving and generating) "Retrieval-Augmented Generation (RAG) is a technique that combines a retriever and a generator to answer questions based on a private knowledge base."
    3.  **User:** "How is that different from fine-tuning?"

**Your Task: Design the Pseudocode/Logic**

**Logic Requirements:**

1.  **Step 1: Generate a Standalone Query:**
    -   When a new user query comes in, do not immediately embed it.
    -   First, make an LLM call.
    -   **LLM Prompt:**
        -   **Role:** "You are a query rewriting expert."
        -   **Context:** Provide the entire conversation history up to the latest user query.
        -   **Task:** "Rewrite the final user query to be a standalone question that can be understood without the chat history. If the final query is already standalone, just return it as is."
    -   **For the scenario above, the LLM should transform "How is that different from fine-tuning?" into something like "How is Retrieval-Augmented Generation (RAG) different from fine-tuning?"**

2.  **Step 2: Retrieve Documents:**
    -   Take the new, standalone query generated in Step 1.
    -   Generate an embedding for this standalone query.
    -   Use this embedding to perform the similarity search in your vector database.

3.  **Step 3: Generate Final Answer:**
    -   Take the documents retrieved in Step 2.
    -   Make a final LLM call to generate the answer.
    -   **Crucially, this final prompt should include the full conversation history *and* the retrieved documents** to ensure the final answer is contextually appropriate and grounded.

**Output Format:**
Provide a detailed, step-by-step description of this iterative retrieval pipeline. Explain why generating a standalone query is the key to making RAG work in a conversational setting.
