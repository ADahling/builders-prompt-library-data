---
title: "Creating a 'Chain of Density' Summarization Agent"
slug: creating-a-chain-of-density-summarization-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 86
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-chain-of-density-summarization-agent
---
# Creating a 'Chain of Density' Summarization Agent

Get a Python script that repeatedly adds details to a document summary without increasing its length, printing each refinement stage.

Variables: article_text, current_summary

## Prompt

Implement the "Chain of Density" (CoD) summarization technique. This method aims to create a high-quality summary by iteratively increasing its density (the amount of information) without increasing its length.

**The CoD Workflow:**

1.  **Input:** A long article or document (`{{article_text}}`).
2.  **Initial Summary:** Generate a very brief, one-sentence summary of the article.
3.  **Iterative Refinement Loop (e.g., 3-5 times):**
    *   **The Prompt:** Create a prompt that takes the `{{current_summary}}` and the original `{{article_text}}`.
    *   The prompt should instruct the LLM to: "Rewrite the following summary to be more dense by adding more key details from the original article. Do not make the summary longer than the original summary. Identify 1-3 entities or details from the article that are missing from the current summary and could be added."
    *   The LLM generates a new, denser summary.
    *   This new summary becomes the `current_summary` for the next iteration.

**Your Task:**

Write a Python script that implements this iterative summarization loop. The script should call the LLM multiple times, with each call refining the summary from the previous step.

**Output:**

A Python script that, when run, prints the summary at each stage of the refinement process, showing how it becomes more detailed over time.
