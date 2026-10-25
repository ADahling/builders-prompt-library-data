---
title: "Agentic System for Personalized Learning Paths"
slug: agentic-system-for-personalized-learning-paths
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-system-for-personalized-learning-paths
---
# Agentic System for Personalized Learning Paths

Get a Python agent pipeline that creates a seven-day Markdown study plan with resources and a project matched to a topic and skill level.

Variables: topic, skill_level

## Prompt

Design a multi-agent system that creates a personalized learning path for a student on a given topic.

**The Goal:**

Create a one-week study plan for a student who wants to learn about `{{topic}}` and is currently at a `{{skill_level}}` (e.g., beginner, intermediate).

**The Agent Crew:**

1.  **Curriculum Designer Agent:**
    *   **Task:** Based on the topic and skill level, create a high-level, day-by-day curriculum. (e.g., Day 1: Introduction, Day 2: Core Concepts, etc.).
2.  **Resource Finder Agent:**
    *   **Task:** For each day in the curriculum, find 2-3 high-quality online resources (articles, videos, tutorials) that are appropriate for the student's skill level.
3.  **Project Idea Agent:**
    *   **Task:** At the end of the week, suggest a small project that the student can build to practice what they've learned.

**The Orchestration:**

Write a Python script that runs this three-agent pipeline. The final output should be a complete, day-by-day study plan.

**Output Format:**

A Markdown file that outlines the 7-day study plan, including the topic for each day, links to the resources, and the final project suggestion.

**Output:**

A Python script that generates the personalized learning path.
