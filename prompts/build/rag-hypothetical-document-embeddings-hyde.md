---
title: "RAG: Hypothetical Document Embeddings (HyDE)"
slug: rag-hypothetical-document-embeddings-hyde
stage: Build
category: "LLM & AI Integration"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/rag-hypothetical-document-embeddings-hyde
---
# RAG: Hypothetical Document Embeddings (HyDE)

Architect a RAG pipeline logic that enhances retrieval accuracy by generating and embedding a hypothetical answer before querying vector data.

## Prompt

Act as an AI researcher implementing an advanced Retrieval-Augmented Generation (RAG) strategy called Hypothetical Document Embeddings (HyDE). The core idea of HyDE is to first generate a hypothetical answer to the user's query, and then use the embedding of that *hypothetical answer* to perform the similarity search, which often provides better results than using the embedding of the query itself.

Your task is to design the pseudocode/logic for a RAG pipeline that implements the HyDE technique.

**Your Task: Design the Pseudocode/Logic**
You are not writing full Python code, but the detailed logic for a function `hyde_rag_query(query: str)`.

**Logic Requirements:**

1.  **Step 1: Generate Hypothetical Document:**
    -   Take the user's `query`.
    -   Make an API call to a fast, creative LLM (e.g., Claude Sonnet 5 or a similar model).
    -   The prompt to this model should be: "Please write a short, one-paragraph document that you believe would perfectly answer the following question: [user's query]".
    -   The model's response is your `hypothetical_document`.

2.  **Step 2: Embed Hypothetical Document:**
    -   Generate a vector embedding for the `hypothetical_document` using a standard bi-encoder model (e.g., `all-MiniLM-L6-v2`). This is your `query_embedding`.

3.  **Step 3: Retrieve Real Documents:**
    -   Perform a similarity search against your vector database using the `query_embedding` from the previous step.
    -   Retrieve the top 5 most similar *real* documents from your knowledge base.

4.  **Step 4: Augmentation and Final Generation:**
    -   Construct a final prompt for a powerful generator LLM (like GPT-5).
    -   This prompt should include the *original user query* and the content of the top 3-5 *real documents* you just retrieved.
    -   Make the final API call and return the model's answer.

**Output Format:**
Provide a well-commented block of pseudocode or a detailed, step-by-step description of the function's logic. Explain the intuition behind HyDE: that a plausible answer is more semantically similar to other good answers than a question is.
