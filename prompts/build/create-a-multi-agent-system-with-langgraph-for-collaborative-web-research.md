---
title: "Create a Multi-Agent System with LangGraph for Collaborative Web Research"
slug: create-a-multi-agent-system-with-langgraph-for-collaborative-web-research
stage: Build
category: "AI Agent Development"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-multi-agent-system-with-langgraph-for-collaborative-web-research
---
# Create a Multi-Agent System with LangGraph for Collaborative Web Research

Architect a collaborative multi-agent LangGraph system to automate iterative web research, reporting, and critical review workflows.

Variables: research_topic

## Prompt

As a senior AI engineer, design and implement a multi-agent system using LangGraph to perform collaborative web research on a given topic. The system should consist of three distinct agents: a Researcher, a Writer, and a Critic.

**System Architecture:**

1.  **State:** Define a shared state graph that includes the research topic, a list of gathered articles, a draft of the report, and feedback from the critic.
2.  **Agents:**
    *   **Researcher Agent:** This agent is responsible for searching the web for relevant articles on the `{{research_topic}}`. It should use a search tool (e.g., TavilySearch) to find at least 5 high-quality sources.
    *   **Writer Agent:** This agent takes the articles gathered by the Researcher and writes a comprehensive report. The report should be at least 500 words and synthesize the information from the sources.
    *   **Critic Agent:** This agent reviews the report written by the Writer. It checks for factual accuracy, clarity, and completeness. It provides specific feedback for revision.
3.  **Graph Flow:**
    *   The graph starts with the Researcher agent.
    *   Once the Researcher has gathered sources, the flow passes to the Writer agent.
    *   After the Writer completes the draft, the Critic agent reviews it.
    *   The graph should loop back to the Writer for revision based on the Critic's feedback. The loop should continue until the Critic approves the report.

**Technical Requirements:**

*   Use Python with the `langgraph` and `langchain` libraries.
*   Define each agent as a node in the graph.
*   Use conditional edges to control the flow based on the Critic's feedback.
*   The final output should be the approved research report in Markdown format.

**Input:**

*   `{{research_topic}}`: A string describing the topic to be researched (e.g., "The future of autonomous AI agents").
