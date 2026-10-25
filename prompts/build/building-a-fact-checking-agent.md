---
title: "Building a 'Fact-Checking' Agent"
slug: building-a-fact-checking-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-fact-checking-agent
---
# Building a 'Fact-Checking' Agent

Get a Python fact-checking agent script and sample verdict that break statements into claims, search sources, and explain cited conclusions.

Variables: statement

## Prompt

Design an agent that can fact-check a given statement. The agent should use a search tool to find credible sources and then compare the statement against the information it finds.

**Agent Workflow:**

1.  **Input:** A statement to be fact-checked, e.g., "{{statement}}".
2.  **Decomposition:** The agent should first break down the statement into searchable claims.
3.  **Search:** For each claim, the agent uses a `web_search` tool to find relevant articles or documents.
4.  **Analysis:** The agent reads the content of the search results and compares it to the original statement.
5.  **Synthesis:** The agent provides a final verdict: "True", "False", or "Uncertain". It must also provide a brief explanation and cite the sources it used.

**Implementation:**

*   This requires a ReAct-style agent with a robust `web_search` tool (e.g., using Tavily or a similar API).
*   The system prompt is critical. It must instruct the agent to be skeptical, to prioritize credible sources (like news organizations, academic institutions), and to provide citations for its conclusion.

**Your Task:**

Write a Python script that sets up this fact-checking agent. You can mock the search tool for simplicity if needed. The script should run the agent on a sample statement and produce a structured verdict.

**Output:**

A Python script for the agent and a sample output in Markdown showing the verdict, explanation, and sources.
