---
title: "Agentic Task Decomposition"
slug: agentic-task-decomposition
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-task-decomposition
---
# Agentic Task Decomposition

Get a Python script that uses an LLM planner to break a high-level objective into actionable steps and print them as a JSON array.

Variables: app_name

## Prompt

Create an agent that can take a high-level, multi-step task and decompose it into a sequence of smaller, actionable steps. This "planner" agent is a crucial component of more complex agentic systems.

**The Task:**

Given a high-level objective like, "Build and deploy a simple landing page for my new app, {{app_name}}.", the agent should produce a step-by-step plan.

**Implementation:**

This is a prompt engineering task.

*   **The Prompt:**
    *   **Role:** "You are an expert project manager and software developer."
    *   **Task:** "Decompose the following objective into a detailed, step-by-step plan. The steps should be clear and actionable."
    *   **Output Format:** "Your output must be a JSON array of strings, where each string is a step in the plan."

**Example Output:**

```json
[
  "1. Write the HTML structure for the landing page.",
  "2. Style the page using CSS, ensuring it is responsive.",
  "3. Write a JavaScript file for any interactive elements.",
  "4. Set up a simple web server to host the files.",
  "5. Deploy the website to a static hosting service like Netlify or Vercel."
]
```

**Your Task:**

Write a Python script that takes a high-level objective, uses an LLM with your planner prompt to generate the plan, and then prints the structured plan.

**Output:**

A Python script that demonstrates this task decomposition.
