---
title: "Implementing Safety Guardrails for an AI Agent"
slug: implementing-safety-guardrails-for-an-ai-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-safety-guardrails-for-an-ai-agent
---
# Implementing Safety Guardrails for an AI Agent

Build a Python AI agent class with input and output moderation, keyword-based topic restrictions, and refusal or fallback responses.

Variables: restricted_topics, user_input

## Prompt

Your task is to implement safety guardrails for an AI agent to prevent it from generating harmful, unethical, or inappropriate content. You will create a system that moderates both the user's input and the agent's output.

**Guardrail Components:**

1.  **Input Moderation:**
    *   Before processing any user input, pass it through a content moderation API (like OpenAI's Moderation endpoint or a self-hosted model).
    *   If the input is flagged for any safety violations (e.g., hate speech, self-harm), the agent should refuse to process it and respond with a polite refusal message.
2.  **Output Moderation:**
    *   After the LLM generates a response but before it's sent to the user, perform another moderation check.
    *   If the agent's response is flagged, do not send it. Instead, you can either:
        *   Generate a new response.
        *   Respond with a generic, safe message (e.g., "I'm sorry, I can't respond to that.").
3.  **Topic Restriction:**
    *   Implement a keyword-based filter to prevent the agent from discussing certain sensitive or off-limits topics defined in a `{{restricted_topics}}` list.
    *   The list could include topics like politics, religion, or illegal activities.

**Implementation:**

*   Create a Python class for your agent.
*   In the agent's main response-generation method, add the input and output moderation steps.
*   Write a function that checks for restricted keywords in the input and output.

**Input:**

*   `{{user_input}}`: The text input from the user.
*   `{{restricted_topics}}`: A list of strings representing the topics to be avoided.

**Output:**

A safe and appropriate response from the agent, or a refusal message if the input or generated output violates the safety policies.
