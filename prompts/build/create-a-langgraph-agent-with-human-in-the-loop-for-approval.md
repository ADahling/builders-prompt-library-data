---
title: "Create a LangGraph Agent with Human-in-the-Loop for Approval"
slug: create-a-langgraph-agent-with-human-in-the-loop-for-approval
stage: Build
category: "AI Agent Development"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-langgraph-agent-with-human-in-the-loop-for-approval
---
# Create a LangGraph Agent with Human-in-the-Loop for Approval

Build a Python LangGraph agent that proposes file deletion, pauses for human approval, and executes or cancels based on the response.

Variables: file_path

## Prompt

Build an AI agent system using LangGraph that requires human approval before executing a critical action. This pattern is essential for creating safe and reliable agents that handle sensitive tasks.

**Scenario:**

An agent is tasked with deleting a file from the file system. Before it can perform the deletion, it must ask for and receive explicit approval from a human user.

**Graph Structure:**

1.  **Initial Node:** The agent starts with a goal, e.g., "Delete the file at {{file_path}}".
2.  **Propose Action Node:** The agent reasons about the goal and proposes an action: `delete_file('{{file_path}}')`. This proposal is added to the shared state.
3.  **Wait for Approval Node:** The graph transitions to a special "wait" node. This node effectively pauses the agent's execution until human input is provided. The system should prompt the user with "Do you approve the action: `delete_file('{{file_path}}')`? (yes/no)".
4.  **Conditional Edge:** Based on the user's input, a conditional edge decides the next step:
    *   If "yes", the graph transitions to the `execute_action` node.
    *   If "no", the graph transitions to an `end` node, and the action is cancelled.
5.  **Execute Action Node:** If approved, this node executes the `delete_file` tool.
6.  **End Node:** The process terminates.

**Your Task:**

Implement this graph using Python and `langgraph`. You will need to:

*   Define the state graph, including a field for the proposed action and the human's response.
*   Create the nodes as functions.
*   Implement the `wait_for_human_input` logic, which will likely involve a `input()` call in a simple script.
*   Set up the conditional edge to route the flow based on the approval status.

**Output:**

A Python script that demonstrates this human-in-the-loop workflow. When run, it should prompt the user for approval before proceeding with the simulated file deletion.
