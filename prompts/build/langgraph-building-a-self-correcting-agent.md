---
title: "LangGraph: Building a Self-Correcting Agent"
slug: langgraph-building-a-self-correcting-agent
stage: Build
category: "AI Agent Development"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/langgraph-building-a-self-correcting-agent
---
# LangGraph: Building a Self-Correcting Agent

Build a LangGraph article-summary agent with state, generation and review nodes, and conditional rewrites based on critic feedback.

Variables: article_text

## Prompt

Design an agent using LangGraph that can reflect on its own work and correct it if it's not good enough. This is a powerful pattern for improving the quality of an agent's output.

**Scenario:**

An agent is tasked with writing a short summary of an article. After writing the summary, it should review it against a set of criteria and decide if it needs to be rewritten.

**Graph Flow:**

1.  **State:** The graph's state should include the original article, the current summary, and a review score.
2.  **Generate Summary Node:** This node takes the article and writes the first draft of the summary.
3.  **Review Summary Node:** This node acts as a critic. It takes the summary and evaluates it based on criteria like:
    *   Does it capture the main points?
    *   Is it concise?
    *   Is it well-written?
    It then gives the summary a score (e.g., "good" or "bad").
4.  **Conditional Edge:** After the review, a conditional edge checks the score:
    *   If the score is "good", the graph transitions to the `end` node.
    *   If the score is "bad", the graph transitions back to the `Generate Summary` node, but this time with the feedback from the review, so it can improve the summary.

**Your Task:**

*   Implement this self-correcting loop using `langgraph`.
*   Define the state, the nodes, and the conditional edge.
*   The "review" can be done by a separate LLM call with a specific prompt that asks it to act as a critic.

**Input:**

*   `{{article_text}}`: A piece of text to be summarized.

**Output:**

A Python script that implements the graph and, when run, shows the agent potentially rewriting the summary at least once before producing the final, approved version.
