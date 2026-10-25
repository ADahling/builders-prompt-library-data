---
title: "Using Few-Shot Prompting with Agents"
slug: using-few-shot-prompting-with-agents
stage: Build
category: "AI Agent Development"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/using-few-shot-prompting-with-agents
---
# Using Few-Shot Prompting with Agents

Get a Python script that builds a few-shot prompt and uses it in an agent chain to address incorrect JSON tool-call formatting.

## Prompt

Improve the reliability of an agent's tool usage by incorporating few-shot examples into its system prompt. This technique helps the LLM understand exactly how to format its tool requests.

**The Problem:**

Sometimes an agent struggles to output the correct JSON format for a tool call, especially with complex schemas or weaker LLMs.

**The Solution:**

Provide examples of successful interactions in the prompt.

**Implementation:**

1.  **Define a Tool:** Create a tool that takes multiple arguments, e.g., `create_calendar_event(title: str, date: str, duration_minutes: int)`.
2.  **Create Few-Shot Examples:** Write out 2-3 examples of a user query and the corresponding correct tool call.
    *   *Example 1:*
        *   User: "Book a 30-minute sync with the team tomorrow."
        *   Agent Action: `{"name": "create_calendar_event", "arguments": {"title": "Team Sync", "date": "tomorrow", "duration_minutes": 30}}`
3.  **Construct the Prompt:**
    *   Start with the base system instructions.
    *   Append the few-shot examples clearly labeled.
    *   End with the actual user input.
4.  **Run the Agent:** Test the agent to see if the few-shot examples improve its formatting accuracy.

**Output:**

A Python script that clearly shows the construction of the few-shot prompt and its use in an agent chain.
