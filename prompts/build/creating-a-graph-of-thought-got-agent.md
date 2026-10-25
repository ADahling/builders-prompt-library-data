---
title: "Creating a Graph-of-Thought (GoT) Agent"
slug: creating-a-graph-of-thought-got-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-graph-of-thought-got-agent
---
# Creating a Graph-of-Thought (GoT) Agent

Get a Python script that explores multiple perspectives on a complex question through LLM calls and synthesizes a balanced recommendation.

Variables: tech_stack_1, tech_stack_2

## Prompt

Implement a basic version of the "Graph-of-Thought" (GoT) reasoning pattern. This advanced technique allows an agent to explore multiple reasoning paths simultaneously and merge them, creating a more robust and comprehensive answer.

**The Concept:**

Instead of a linear chain of thought (Thought -> Action -> ...), GoT allows the agent to generate multiple "thoughts" at each step. These thoughts can be explored in parallel, and their results can be combined or synthesized later.

**Simplified Implementation:**

1.  **The Task:** A complex question, e.g., "Should our company migrate from {{tech_stack_1}} to {{tech_stack_2}}?"
2.  **Thought Generation:**
    *   In the first step, prompt an LLM to generate multiple, distinct perspectives or sub-questions to explore. For our example, it might generate:
        *   "What are the performance benefits of {{tech_stack_2}}?"
        *   "What is the developer learning curve for {{tech_stack_2}}?"
        *   "What are the long-term costs of migrating?"
3.  **Parallel Exploration:**
    *   For each of these generated thoughts, run a separate agent or search query to find the answer.
4.  **Synthesis:**
    *   In the final step, feed all the individual answers into a final LLM call. The prompt for this call should be to synthesize all the information into a single, balanced recommendation.

**Your Task:**

Write a Python script that orchestrates this process. You will need multiple LLM calls: one for thought generation, several for exploration, and one for the final synthesis.

**Output:**

A Python script that demonstrates the GoT flow, printing the output of each stage.
