---
title: "Agentic Project Management Assistant"
slug: agentic-project-management-assistant
stage: Build
category: "AI Agent Development"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-project-management-assistant
---
# Agentic Project Management Assistant

Get a Python prompt chain and sample project plan that break a goal into tasks, prioritize them, and assign team members based on skills.

Variables: team_members_and_skills, project_goal

## Prompt

Design an AI agent that acts as a project management assistant. It should be able to take a project goal, break it down into tasks, and assign them to team members.

**Agent's Capabilities:**

1.  **Task Decomposition:** Given a project goal, break it down into a list of smaller, actionable tasks.
2.  **Task Prioritization:** Estimate the effort for each task and suggest a priority (e.g., High, Medium, Low).
3.  **Task Assignment:** Given a list of team members and their skills (`{{team_members_and_skills}}`), suggest which team member would be best suited for each task.

**Implementation:**

This can be implemented as a multi-step prompt chain.

*   **Step 1 (Decomposition):** Prompt an LLM to break down the `{{project_goal}}` into tasks.
*   **Step 2 (Prioritization):** Prompt an LLM to take the list of tasks and add a priority level to each.
*   **Step 3 (Assignment):** Prompt an LLM with the prioritized tasks and the list of team members, and ask it to assign each task.

**Your Task:**

Write a Python script that runs this chain of prompts. The output of each step should be fed into the next. The final output should be a structured JSON object or Markdown table showing the tasks, their priorities, and their assignees.

**Output:**

A Python script and a sample project plan in Markdown.
