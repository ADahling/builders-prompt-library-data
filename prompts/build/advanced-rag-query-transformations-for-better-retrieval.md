---
title: "Advanced RAG: Query Transformations for Better Retrieval"
slug: advanced-rag-query-transformations-for-better-retrieval
stage: Build
category: "LLM & AI Integration"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-query-transformations-for-better-retrieval
---
# Advanced RAG: Query Transformations for Better Retrieval

Implement a query transformation pipeline using multi-query expansion and re-ranking to optimize document retrieval for complex RAG tasks.

## Prompt

Act as an AI researcher designing a more robust RAG system. You've observed that user queries are often not optimal for vector search. For example, they might be too short, or they might ask multiple questions at once. You decide to implement a 'query transformation' step to improve retrieval accuracy.

Your task is to design the logic for a query transformation module that uses an LLM to rewrite the user's query before it's embedded.

**Your Task: Design the Pseudocode/Logic**

**Logic Requirements:**

**The Core Idea:** Before embedding the user's query, send it to an LLM to generate several new, potentially better queries.

**The LLM Prompt:**
-   **Role:** "You are an expert query optimizer for a semantic search system."
-   **Context:** "The user's query will be used to find relevant documents in a vector database."
-   **Task:** "Given the following user query, generate a set of 3-5 transformed queries that might improve retrieval results. Consider the following transformations:"
    -   **1. Rewrite as a Statement:** If the query is a question, rewrite it as a statement that a document answering it might contain (this is similar to HyDE).
    -   **2. Decompose Sub-Questions:** If the query contains multiple questions, break it down into several smaller, single-focus questions.
    -   **3. Add Related Terms:** Expand the query with synonyms or related technical terms.
-   **User Query:** "[User Query]"
-   **Output Format:** "Return a JSON object with a single key, 'transformed_queries', containing a list of the new query strings."

**The Workflow:**
1.  **Get User Query:** e.g., "What is RAG and how does it differ from fine-tuning?"
2.  **Call Query Transformer LLM:** Send this query to the LLM with the prompt above.
3.  **Receive Transformed Queries:** The LLM might return:
    `{
      "transformed_queries": [
        "Retrieval-Augmented Generation (RAG) is a technique to improve LLM answers.",
        "The difference between Retrieval-Augmented Generation and fine-tuning.",
        "What is Retrieval-Augmented Generation (RAG)?",
        "How is RAG different from fine-tuning an LLM?",
        "RAG vs fine-tuning for custom knowledge bases."
      ]
    }`
4.  **Multi-Query Retrieval:**
    -   Generate embeddings for *all* the transformed queries (and the original one).
    -   Perform multiple searches in your vector database, one for each embedding.
    -   Collect all the retrieved documents, de-duplicate them, and re-rank them based on relevance.
5.  **Generate Final Answer:** Pass the top-ranked, retrieved documents to your generator LLM.

**Output Format:**
Provide a detailed, step-by-step description of this query transformation pipeline.
