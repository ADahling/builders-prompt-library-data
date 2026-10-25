---
title: "Multi-Agent Orchestration: Debate Simulation"
slug: multi-agent-orchestration-debate-simulation
stage: Build
category: "AI Agent Development"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/multi-agent-orchestration-debate-simulation
---
# Multi-Agent Orchestration: Debate Simulation

Build a debate simulation on a chosen topic with proponent and opponent agents, a moderator, alternating turns, and a closing summary.

Variables: topic

## Prompt

Create a simulation of a debate between two AI agents on a given topic. A third agent will act as a moderator.

**Agent Roles:**

1.  **Agent For (Proponent):**
    *   This agent will argue in favor of the `{{topic}}`.
    *   Its persona should be configured to be positive and persuasive.
2.  **Agent Against (Opponent):**
    *   This agent will argue against the `{{topic}}`.
    *   Its persona should be configured to be critical and skeptical.
3.  **Moderator Agent:**
    *   This agent manages the debate.
    *   It starts by introducing the topic.
    *   It gives each agent a turn to speak.
    *   It ensures the debate stays on topic and is civil.
    *   It concludes the debate with a summary.

**Implementation Strategy:**

This can be implemented in a few ways. A good approach is a custom Python loop:

1.  Initialize the three agents. You can use a standard LLM chain for each, but with different system prompts to define their roles and stances.
2.  The Moderator starts with an opening statement.
3.  The loop then alternates between the Proponent and Opponent for a fixed number of turns (e.g., 3 rounds).
4.  In each turn, the current speaker receives the history of the debate so far and adds its argument.
5.  After the rounds are complete, the Moderator makes a closing statement, summarizing the key points from both sides.

**Input:**

*   `{{topic}}`: The topic of the debate (e.g., "Should AI be regulated?").

**Output:**

The full transcript of the debate, showing the statements from the Moderator and each of the debating agents in order.
