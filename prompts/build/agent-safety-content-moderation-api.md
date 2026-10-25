---
title: "Agent Safety: Content Moderation API"
slug: agent-safety-content-moderation-api
stage: Build
category: "AI Agent Development"
grade: C
score: 63
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/agent-safety-content-moderation-api
---
# Agent Safety: Content Moderation API

Get a Python wrapper for an AI agent that checks user input and agent output with a moderation API as part of its safety workflow.

Variables: user_input

## Prompt

Integrate a content moderation API into an AI agent's workflow to ensure that it does not process or generate unsafe content. This is a critical step in building responsible AI systems.

**Your Task:**

Create a Python function that acts as a wrapper around your agent's main logic. This function will perform moderation checks before and after the agent runs.

**Moderation Workflow:**

1.  **Input Moderation:**
    *   Take the `{{user_input}}`.
    *   Send it to OpenAI's Moderation endpoint (or a similar service).
    *   Check the response for any flagged categories (e.g., `hate
