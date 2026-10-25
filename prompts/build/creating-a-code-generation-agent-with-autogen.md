---
title: "Creating a Code Generation Agent with AutoGen"
slug: creating-a-code-generation-agent-with-autogen
stage: Build
category: "AI Agent Development"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-code-generation-agent-with-autogen
---
# Creating a Code Generation Agent with AutoGen

Set up AutoGen coder and executor agents in Python, with a working directory and an initial chat for a problem requiring code.

## Prompt

Use AutoGen to create a pair of agents that collaborate to write and execute Python code to solve a problem.

**Agent Roles:**

1.  **Assistant Agent:**
    *   This is the "coder" agent.
    *   It receives a problem description and writes Python code to solve it.
2.  **User Proxy Agent:**
    *   This agent acts as the "executor" and represents the user.
    *   It receives the code from the Assistant Agent.
    *   Crucially, it is configured to execute the code it receives.
    *   It then reports the result of the execution back to the Assistant Agent.

**Workflow:**

1.  The user gives a task to the User Proxy Agent, e.g., "What is the 10th Fibonacci number?"
2.  The User Proxy Agent passes this task to the Assistant Agent.
3.  The Assistant Agent writes a Python script to calculate the 10th Fibonacci number and sends the code back.
4.  The User Proxy Agent receives the code, executes it in a code block, and captures the output.
5.  The output (the result of the calculation) is then sent back to the Assistant Agent.
6.  The Assistant Agent sees the result and can then provide the final answer to the user.

**Your Task:**

*   Set up an `AssistantAgent` and a `UserProxyAgent` in Python using the `autogen` library.
*   Configure the `UserProxyAgent` with a `code_execution_config` that specifies a working directory. This enables it to execute code.
*   Initiate a chat between the two agents with a problem that requires code to be written and executed.

**Output:**

The Python script for setting up and running the agents, along with the full conversation history showing the code generation and execution steps.
