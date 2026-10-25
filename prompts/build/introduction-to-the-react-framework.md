---
title: "Introduction to the ReAct Framework"
slug: introduction-to-the-react-framework
stage: Build
category: "AI Agent Development"
grade: A
score: 89
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/introduction-to-the-react-framework
---
# Introduction to the ReAct Framework

Create a beginner-friendly Markdown tutorial explaining the ReAct framework's reasoning loop alongside a runnable LangChain Python example.

Variables: company

## Prompt

You are an AI educator creating a tutorial for beginners on the ReAct (Reasoning and Acting) framework for AI agents. Your goal is to explain the concept clearly and provide a simple, runnable code example.

**Tutorial Content:**

1.  **What is ReAct?**
    *   Explain the core idea of ReAct: combining reasoning (thinking about what to do) and acting (taking action, like using a tool).
    *   Use the analogy of a person thinking "I need to know the weather. I should check my weather app." (Reasoning) and then opening the app (Acting).
    *   Contrast this with simpler agents that might just try to directly answer a question without a thought process.
2.  **The ReAct Loop:**
    *   Describe the typical ReAct loop: **Thought -> Action -> Observation -> Thought ...**
    *   **Thought:** The LLM thinks about the problem and decides on the next action.
    *   **Action:** The agent executes the action (e.g., calls a tool).
    *   **Observation:** The agent gets the result of the action.
    *   The loop repeats until the agent has the final answer.
3.  **Simple Code Example:**
    *   Provide a very simple Python code example using LangChain's `ReActAgent`.
    *   The agent should have only one tool: a `search` tool that simulates searching the web (it can just return a fixed string).
    *   The example should show how to define the tool, initialize the agent, and run it with a simple question like "Who is the CEO of {{company}}?".

**Output Format:**

A Markdown file containing the tutorial. The code block for the example should be complete and runnable after installing the necessary libraries (`langchain
