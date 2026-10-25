---
title: "Creating a 'Tree of Thoughts' (ToT) Agent"
slug: creating-a-tree-of-thoughts-tot-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-tree-of-thoughts-tot-agent
---
# Creating a 'Tree of Thoughts' (ToT) Agent

Implement a simplified version of the "Tree of Thoughts" ToT agentic reasoning framework.

Variables: city_A, city_B

## Prompt

Implement a simplified version of the "Tree of Thoughts" (ToT) agentic reasoning framework. ToT allows an agent to explore multiple reasoning paths (branches) and self-evaluate them, pruning bad branches and pursuing promising ones.

**The Concept:**

1.  **Decomposition:** Break a problem into smaller steps.
2.  **Thought Generation:** For each step, generate multiple possible "thoughts" or approaches.
3.  **Evaluation:** Use an LLM to evaluate each thought, giving it a score (e.g., "sure", "likely", "impossible").
4.  **Search:** Explore the most promising thoughts in a tree-like structure. If a path leads to a dead end, backtrack and try another branch.

**Simplified Implementation:**

*   **Task:** A simple planning task, e.g., "How can I get from my home in {{city_A}} to a meeting in {{city_B}} by tomorrow morning?"
*   **Step 1 (Generate Initial Thoughts):** Prompt an LLM to generate 3-5 high-level travel options (e.g., "Fly", "Drive", "Take a train").
*   **Step 2 (Evaluate Thoughts):** For each option, prompt an LLM to evaluate its feasibility. The prompt should ask for a score and a brief reason.
*   **Step 3 (Expand Best Thought):** Choose the best option (e.g., "Fly") and generate sub-steps for it (e.g., "1. Book a flight. 2. Book a taxi to the airport...").

**Your Task:**

Write a Python script that orchestrates these three steps. It will involve multiple LLM calls to simulate the generation, evaluation, and expansion phases of the ToT process.

**Output:**

A Python script that demonstrates this simplified ToT workflow, printing the generated thoughts, their evaluations, and the final expanded plan.
