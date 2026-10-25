---
title: "Using LangSmith for Agent Observability"
slug: using-langsmith-for-agent-observability
stage: Build
category: "AI Agent Development"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/using-langsmith-for-agent-observability
---
# Using LangSmith for Agent Observability

Get a LangSmith guide for debugging agents, with setup steps, trace interpretation, latency and token tracking, and a practical example.

## Prompt

Create a guide on how to use LangSmith for observability into your AI agents. Observability is key to understanding, debugging, and improving agent performance.

**Guide Sections:**

1.  **What is LangSmith and Why Use It?**
    *   Describe LangSmith as a platform for debugging, testing, evaluating, and monitoring LLM applications.
    *   Explain the key benefit: it gives you a detailed, step-by-step trace of your agent's execution, showing every thought, tool call, and LLM interaction.
2.  **Getting Started (Setup):**
    *   Show the simple setup process:
        *   Sign up for LangSmith.
        *   Get an API key.
        *   Set the required environment variables in your Python environment:
            *   `LANGCHAIN_TRACING_V2="true"`
            *   `LANGCHAIN_ENDPOINT="https://api.smith.langchain.com"`
            *   `LANGCHAIN_API_KEY="..."`
            *   `LANGCHAIN_PROJECT="..."` (to organize runs)
3.  **Reading a Trace:**
    *   Explain the main components of a LangSmith trace:
        *   **Root Span:** The overall agent run.
        *   **Child Spans:** The individual steps within the run (e.g., LLM calls, tool calls, parsers).
        *   **Inputs and Outputs:** You can inspect the exact inputs and outputs of every step.
        *   **Latency and Token Counts:** LangSmith automatically tracks how long each step took and how many tokens were used.
4.  **A Practical Example:**
    *   Take a simple ReAct agent (e.g., one with a calculator tool).
    *   Run it with the LangSmith environment variables set.
    *   Include a screenshot of what the resulting trace looks like in the LangSmith UI (you can describe it in text).
    *   Point out how the trace clearly shows the "Thought -> Action -> Observation" loop.

**Output Format:**

A Markdown document that serves as a practical introduction to LangSmith for developers building AI agents.
