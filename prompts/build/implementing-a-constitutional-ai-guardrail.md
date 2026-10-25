---
title: "Implementing a 'Constitutional AI' Guardrail"
slug: implementing-a-constitutional-ai-guardrail
stage: Build
category: "AI Agent Development"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-a-constitutional-ai-guardrail
---
# Implementing a 'Constitutional AI' Guardrail

Build a Python agent guardrail that drafts a response, critiques it against a constitution, and revises it, with a sample violating query.

## Prompt

Implement a "Constitutional AI" guardrail for an agent. This technique, popularized by Anthropic, involves providing the agent with a set of principles or a "constitution" that it must follow when generating responses. It's a powerful way to steer an agent's behavior without complex moderation rules.

**The Process:**

1.  **The Constitution:** Write a short constitution (a list of principles) for your agent. For example:
    *   Principle 1: Be helpful and harmless.
    *   Principle 2: Do not give financial advice.
    *   Principle 3: If asked about a sensitive topic, respond with "I am unable to discuss that topic."
2.  **The Two-Step Prompting:**
    *   **Step 1 (Initial Response):** First, prompt the LLM with the user's query to get an initial response.
    *   **Step 2 (Critique and Revise):** Then, create a second prompt. This prompt includes the original query, the initial response, and your constitution. It asks the LLM to critique the initial response based on the constitution and then generate a revised, compliant response.

**Your Task:**

Write a Python function that takes a user query and implements this two-step "critique and revise" process. The function should return the final, constitutionally-compliant response.

**Output:**

A Python script demonstrating this process. Test it with a query that would violate the constitution (e.g., "Should I invest in Bitcoin?") to show that the final response is a safe refusal.
