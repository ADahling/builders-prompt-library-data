---
title: "Building a Research Agent with CrewAI"
slug: building-a-research-agent-with-crewai
stage: Build
category: "AI Agent Development"
grade: C
score: 61
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-research-agent-with-crewai
---
# Building a Research Agent with CrewAI

Build a CrewAI researcher with a search tool, persona, and task to find at least three credible sources and extract key findings on a topic.

Variables: topic

## Prompt

Your goal is to create a research agent using the CrewAI framework. This agent will be part of a crew designed to research a topic, write a report, and present it.

**Crew Composition:**

*   **Researcher:** An agent responsible for finding information on a given topic.
*   **Writer:** An agent that takes the research findings and writes a detailed report.

**Task for this Prompt:**

Focus on implementing the **Researcher** agent. This agent should:

1.  **Have a clear goal:** To research the `{{topic}}` and find relevant, up-to-date information.
2.  **Have a backstory:** Define a persona for the agent, such as "A seasoned research analyst with a knack for finding hidden gems of information."
3.  **Use a specific tool:** Integrate a search tool like DuckDuckGo Search (`ddg-search`) to perform the research.
4.  **Define a task:** The agent's task is to find at least 3 credible sources (articles, papers, etc.) on the `{{topic}}` and extract the key findings from each.

**Implementation using CrewAI:**

1.  Import `Agent
