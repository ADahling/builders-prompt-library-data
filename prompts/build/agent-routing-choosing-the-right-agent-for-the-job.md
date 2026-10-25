---
title: "Agent Routing: Choosing the Right Agent for the Job"
slug: agent-routing-choosing-the-right-agent-for-the-job
stage: Build
category: "AI Agent Development"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agent-routing-choosing-the-right-agent-for-the-job
---
# Agent Routing: Choosing the Right Agent for the Job

Get a Python routing demo where a supervisor LLM directs user requests to math, search, or creative workers in a multi-agent system.

Variables: user_query

## Prompt

Implement a routing system where a "Supervisor" agent receives a user request and decides which specialized "Worker" agent should handle it. This is a common pattern for building scalable, multi-domain AI systems.

**The Setup:**

1.  **Worker Agents:**
    *   **Math Agent:** Specializes in calculations. Has a calculator tool.
    *   **Search Agent:** Specializes in finding current information. Has a web search tool.
    *   **Creative Agent:** Specializes in writing stories or poems. No tools, just a creative system prompt.
2.  **Supervisor Agent (The Router):**
    *   This agent does not answer the user's query directly.
    *   Its job is to analyze the query and output the name of the appropriate worker agent.
    *   You can implement this using an LLM with a custom output parser that forces it to return one of three strings: "math", "search", or "creative".

**The Workflow:**

1.  User submits a query: `{{user_query}}`.
2.  The query goes to the Supervisor.
3.  The Supervisor returns the routing decision.
4.  Your Python code uses an `if/elif` block based on the decision to route the query to the chosen Worker agent.
5.  The Worker agent processes the query and returns the final answer.

**Your Task:**

Write the Python code to implement this routing logic. You don't need to build complex worker agents; simple LLM chains or mock functions will suffice to demonstrate the routing mechanism.

**Output:**

A Python script that clearly demonstrates the Supervisor agent making a routing decision and passing the execution to the correct sub-agent.
