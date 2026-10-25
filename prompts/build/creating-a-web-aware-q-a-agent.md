---
title: "Creating a 'Web-Aware' Q&A Agent"
slug: creating-a-web-aware-q-a-agent
stage: Build
category: "AI Agent Development"
grade: C
score: 65
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-web-aware-q-a-agent
---
# Creating a 'Web-Aware' Q&A Agent

Get a Python script for a ReAct Q&A agent that searches the web for current information and shows its decision to use the search tool.

Variables: company_ticker

## Prompt

Build an agent that can answer questions by first searching the web to get up-to-date information. This combines the power of a search tool with the reasoning of an LLM.

**The Agent:**

This is a classic ReAct agent setup.

1.  **The Tool:** A web search tool. You can use LangChain's built-in `TavilySearchResults` tool or a similar integration. You will need an API key for the search provider.
2.  **The Agent:**
    *   Initialize a ReAct agent using a function like `create_react_agent`.
    *   Provide the search tool to the agent.
    *   The system prompt should encourage the agent to use the search tool whenever it needs current information or is unsure of an answer.

**The Task:**

Ask the agent a question that cannot be answered from its training data, such as:
*   "Who won the last Super Bowl?"
*   "What are the top trending news stories today?"
*   "What is the current stock price of {{company_ticker}}?"

**Expected Behavior:**

The agent should recognize that it needs external information, call the search tool, get the results, and then use those results to formulate its final answer.

**Output:**

A Python script that sets up and runs this web-aware agent. The output should show the agent's decision to use the search tool.
