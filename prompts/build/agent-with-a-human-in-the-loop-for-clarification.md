---
title: "Agent with a Human-in-the-Loop for Clarification"
slug: agent-with-a-human-in-the-loop-for-clarification
stage: Build
category: "AI Agent Development"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agent-with-a-human-in-the-loop-for-clarification
---
# Agent with a Human-in-the-Loop for Clarification

Build an agent that uses an ask_user tool to pause ambiguous tasks, collect clarification in the console, and continue with the user's answer.

## Prompt

Create an AI agent that can pause and ask the user for clarification if it is unsure how to proceed. This makes the agent more robust and interactive.

**Scenario:**

An agent is given a vague task, such as "Summarize the document". The agent has a tool to read a document, but it doesn't know *how* the user wants it summarized (e.g., a single paragraph, bullet points, a 100-word summary).

**Agent's Logic:**

1.  The agent receives the user's request.
2.  It recognizes that the request is ambiguous.
3.  Instead of trying to guess, it responds to the user with a clarifying question: "How would you like me to summarize the document? For example, as a single paragraph or as a list of bullet points?"
4.  The agent then waits for the user's response.
5.  Once the user provides the missing detail, the agent proceeds with the summarization task as specified.

**Implementation Strategy:**

This can be implemented with a ReAct-style agent and a special tool:

1.  **`ask_user` Tool:**
    *   Create a tool named `ask_user` that takes a `question` string as input.
    *   When this tool is called, the agent's execution should print the question to the console and wait for the user to type a response.
    *   The user's response is then returned as the output of the tool.
2.  **Agent Prompt:**
    *   Modify the agent's system prompt to encourage it to use the `ask_user` tool whenever it encounters ambiguity or needs more information.
    *   The prompt should say something like: "If the user's request is unclear, you must use the `ask_user` tool to ask for clarification."

**Your Task:**

Write a Python script that implements this agent. You will need to:

*   Define the `ask_user` tool.
*   Create a ReAct agent with a prompt that encourages clarification.
*   Run the agent with a vague request and show that it asks for clarification before completing the task.

**Output:**

A Python script and a transcript of the interaction, demonstrating the clarification loop.
