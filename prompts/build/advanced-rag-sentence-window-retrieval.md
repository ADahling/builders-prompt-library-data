---
title: "Advanced RAG: Sentence Window Retrieval"
slug: advanced-rag-sentence-window-retrieval
stage: Build
category: "LLM & AI Integration"
grade: C
score: 67
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-sentence-window-retrieval
---
# Advanced RAG: Sentence Window Retrieval

Optimize RAG precision by implementing sentence-level retrieval with surrounding context windows for balanced, high-fidelity LLM inputs.

## Prompt

Act as an AI engineer refining a RAG system. You've found that retrieving individual sentences can be too specific, while retrieving whole paragraphs can be too broad. You decide to implement a 'Sentence Window Retriever' to get more focused context.

**Your Task:** Design the logic for a Sentence Window Retriever pipeline.

**The Core Idea:** When a single sentence is identified as the best match for a query, you retrieve not just that sentence, but also a 'window' of sentences surrounding it (e.g., the 2 sentences before and the 2 sentences after).

**Your Task: Design the Pseudocode/Logic**

**Part 1: The Indexing Pipeline**
1.  **Load Documents:** Start with your collection of documents.
2.  **Split into Sentences:** The key difference is that you split your documents into *individual sentences*. Each sentence is a 'document' in your vector store.
3.  **Store with Metadata:** When you store the embedding for each sentence, you must also store crucial metadata:
    -   `document_id`: The ID of the original source document.
    -   `sentence_index`: The position of this sentence within the original document (e.g., 0, 1, 2, ...).

**Part 2: The Retrieval Pipeline**
1.  **Query:** A user submits a query.
2.  **Search for a Single Sentence:** Perform a similarity search against your vector store. This will retrieve the single best-matching *sentence*.
3.  **Get Metadata:** From the retrieved sentence, extract its `document_id` and its `sentence_index`.
4.  **Build the Window:**
    -   Access the original document using the `document_id`.
    -   Split this original document into its list of sentences.
    -   Go to the `sentence_index` that you found.
    -   Create your context window by taking the sentences from `index - N` to `index + N` (where N is your window size, e.g., 2).
    -   Handle edge cases (e.g., if the best sentence is the very first one, you can't get sentences before it).
5.  **Concatenate and Generate:**
    -   Join the sentences in the window back into a single string of text.
    -   Pass this context window to your generator LLM to get the final answer.

**Output Format:**
Provide a detailed, step-by-step description of this pipeline. Explain why this method provides a better balance of specificity and context than simple chunking.
