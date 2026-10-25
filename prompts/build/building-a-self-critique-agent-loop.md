---
title: "Building a 'Self-Critique' Agent Loop"
slug: building-a-self-critique-agent-loop
stage: Build
category: "AI Agent Development"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-self-critique-agent-loop
---
# Building a 'Self-Critique' Agent Loop

Get a Python script that orchestrates writer and critic LLM calls for a story, then prints the draft, actionable critique, and revision.

## Prompt

Create an agent that improves its own output through a loop of self-critique. The agent will generate a response, then another agent (or the same agent with a different prompt) will critique it, and the first agent will then generate a revised response based on the critique.

**The Workflow:**

1.  **The Task:** A creative writing task, e.g., "Write a short, spooky story about a haunted lighthouse."
2.  **Step 1 (Draft):** The "Writer" agent generates the first draft of the story.
3.  **Step 2 (Critique):** The "Critic" agent receives the draft. Its prompt instructs it to be a harsh but fair literary critic. It should provide specific, actionable feedback (e.g., "The beginning is too slow," "The description of the ghost is not scary enough").
4.  **Step 3 (Revise):** The "Writer" agent receives its original draft *and* the critic's feedback. Its prompt for this step is to "Revise the following story based on the provided critique."

**Your Task:**

Write a Python script that orchestrates this three-step process. You will need to define the prompts for the Writer, the Critic, and the revision step. You can use simple LLM chains for each agent.

**Output:**

A Python script that, when run, prints the initial draft, the critique, and the final, revised story.
