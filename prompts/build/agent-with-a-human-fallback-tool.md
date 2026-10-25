---
title: "Agent with a 'Human Fallback' Tool"
slug: agent-with-a-human-fallback-tool
stage: Build
category: "AI Agent Development"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agent-with-a-human-fallback-tool
---
# Agent with a 'Human Fallback' Tool

Get a Python customer service agent demo that searches FAQs and stops for human handoff when answers are missing or users request help.

## Prompt

Design an agent that tries to solve a problem autonomously but has a specific tool it can call to escalate the issue to a human operator if it gets stuck or if the user requests it.

**Scenario:**

A customer service chatbot.

**Tools:**

1.  `search_faq`: A tool to search a knowledge base.
2.  `escalate_to_human`: A tool that the agent can call. When called, it should stop the agent's execution and return a message indicating that a human will take over.

**Agent Logic:**

*   The agent should always try to use `search_faq` first.
*   If the FAQ doesn't contain the answer, or if the user explicitly says "I want to speak to a human", the agent should use the `escalate_to_human` tool.

**Implementation:**

*   Define the two tools. The `escalate_to_human` tool can just return a specific string like "ESCALATION_TRIGGERED".
*   Create a ReAct agent.
*   Write a custom execution loop. If the agent's output contains "ESCALATION_TRIGGERED", break the loop and print a message to the user: "Transferring you to a human agent..."

**Output:**

A Python script showing the agent attempting to answer a question, failing, and then successfully using the fallback tool.
