---
title: "AI Safety: Detecting and Mitigating Hallucinations in RAG"
slug: ai-safety-detecting-and-mitigating-hallucinations-in-rag
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/ai-safety-detecting-and-mitigating-hallucinations-in-rag
---
# AI Safety: Detecting and Mitigating Hallucinations in RAG

Design a robust verification pipeline to decompose RAG-generated responses and cross-reference individual claims against source documents.

## Prompt

Act as an AI safety engineer working on a Retrieval-Augmented Generation (RAG) system. A major problem is 'hallucination', where the LLM generates facts that are not supported by the retrieved documents. You need to design a system to detect and mitigate this.

Your task is to design the logic for a 'post-processing' step that verifies the LLM's generated answer against the source documents.

**Your Task: Design the Pseudocode/Logic**
You are not writing full Python code, but the detailed logic for a function `verify_rag_answer(original_query, retrieved_docs, generated_answer)`.

**Logic Requirements:**

1.  **Step 1: Deconstruct the Answer:**
    -   Take the `generated_answer` from the RAG system.
    -   Make an API call to a fast LLM (e.g., Claude Sonnet 5).
    -   The prompt should be: "Break down the following text into a list of individual factual claims. Return the output as a JSON array of strings." Pass the `generated_answer` to this prompt.
    -   The result is a `list_of_claims`.

2.  **Step 2: Verify Each Claim:**
    -   Initialize an empty list called `verified_claims`.
    -   Loop through each `claim` in the `list_of_claims`.
    -   For each `claim`
