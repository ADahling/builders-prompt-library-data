---
title: "Managing Agent Costs: Token Tracking"
slug: managing-agent-costs-token-tracking
stage: Build
category: "AI Agent Development"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/managing-agent-costs-token-tracking
---
# Managing Agent Costs: Token Tracking

Get a Python script that tracks LangChain agent token usage and cost per run, with optional guidance on enforcing a token limit.

## Prompt

Implement a mechanism to track and limit the number of tokens (and therefore the cost) consumed by an AI agent during its execution. This is vital for production deployments.

**The Problem:**

Agents can sometimes get stuck in infinite loops or generate excessively long responses, leading to high API bills.

**Implementation (using LangChain):**

1.  **Callbacks:** LangChain provides a callback system that allows you to hook into various stages of the agent's execution.
2.  **Token Usage Callback:** Use the built-in `get_openai_callback` context manager.
3.  **The Setup:**
    *   Create a standard agent (e.g., a ReAct agent with a search tool).
    *   Wrap the agent's execution call (`agent.invoke()`) inside the `with get_openai_callback() as cb:` block.
4.  **Reporting:**
    *   After the agent finishes, print the statistics collected by the callback object (`cb`). This includes total tokens, prompt tokens, completion tokens, and total cost in USD.
5.  **Implementing a Limit (Optional but recommended):**
    *   Show how you could theoretically implement a hard limit. For example, checking the token count after each step in a custom loop and raising an exception if it exceeds a threshold.

**Output:**

A Python script that runs an agent and prints a detailed breakdown of the token usage and cost for that specific run.
