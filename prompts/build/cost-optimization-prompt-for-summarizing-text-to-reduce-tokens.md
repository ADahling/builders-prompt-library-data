---
title: "Cost Optimization: Prompt for Summarizing Text to Reduce Tokens"
slug: cost-optimization-prompt-for-summarizing-text-to-reduce-tokens
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cost-optimization-prompt-for-summarizing-text-to-reduce-tokens
---
# Cost Optimization: Prompt for Summarizing Text to Reduce Tokens

Condense long document chunks into factually dense summaries to reduce token usage and costs in RAG pipelines without losing critical data.

Variables: document_text

## Prompt

You are building a RAG pipeline where you retrieve large documents. Before passing these documents to the final, expensive generator model, you want to use a cheap, fast model to summarize them, reducing the number of tokens sent in the final prompt and thus saving costs.

Your task is to create a highly effective prompt for a fast model (like Claude Sonnet 5 or Gemini 3) to perform this intermediate summarization.

**Scenario:**
- **Input:** A long document chunk (e.g., 2,000 words).
- **Goal:** Create a shorter, but still factually dense, summary that preserves all the key information needed to answer a potential user query.

**Prompt Engineering Task:**
You are not writing code, but the prompt itself.

**Prompt Requirements:**

1.  **Role Definition:** "You are a highly efficient and accurate text compression and summarization engine."

2.  **The Task:** "Your task is to read the following document and create a concise, factually dense summary. The goal is to reduce the token count while losing as little critical information as possible."

3.  **Input Data:** "Here is the document: [{{document_text}}]."

4.  **Key Constraints (The 'Lossless' Instruction):**
    -   "This is a 'lossy' compression, but you must strive to be as 'lossless' as possible regarding factual information."
    -   "**DO NOT** omit any names, dates, numbers, statistics, key findings, or specific technical terms."
    -   "**DO** remove filler words, introductory phrases, redundant explanations, and conversational language."
    -   "Rewrite sentences to be more direct and concise."
    -   "The output should be a dense paragraph of text, not a list of bullet points."

5.  **Final Instruction:** "The purpose of this summary is to serve as context for another AI to answer questions. It is critical that all substantive facts are preserved. Produce only the summary and nothing else."

**Output Format:**
Provide a single block of text representing the complete, final prompt that would be sent to the intermediate summarization model.
