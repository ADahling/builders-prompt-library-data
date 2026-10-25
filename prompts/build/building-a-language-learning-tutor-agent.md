---
title: "Building a Language Learning Tutor Agent"
slug: building-a-language-learning-tutor-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-language-learning-tutor-agent
---
# Building a Language Learning Tutor Agent

Get a Python tutor script and sample conversation for language practice with multi-turn chat, sentence corrections, and grammar explanations.

Variables: target_language

## Prompt

Create an AI agent that acts as a language learning tutor. The agent should be able to have a conversation with a user in a target language, correct their mistakes, and explain grammar rules.

**Agent's Capabilities:**

1.  **Conversational Partner:** Hold a basic conversation in the `{{target_language}}`.
2.  **Error Correction:** Identify grammatical errors or awkward phrasing in the user's input.
3.  **Explanation:** Explain *why* something was a mistake and provide the correct phrasing.

**Implementation:**

This requires a sophisticated system prompt.

*   **The Prompt:**
    *   **Role:** "You are a friendly and patient language tutor for {{target_language}}."
    *   **Task:** "Have a conversation with the user. When the user makes a mistake, you must correct them. Your response should be in two parts: first, the corrected version of the user's sentence, and second, a simple explanation of the grammar rule they broke."
    *   **Output Format:** "Please format your corrections clearly, for example: 'Corrected: [corrected sentence]. Explanation: [grammar explanation].' Then, continue the conversation."

**Your Task:**

Write a Python script that sets up a conversational chain with this detailed prompt. The script should have a loop to allow for a multi-turn conversation.

**Output:**

A Python script for the tutor agent and a sample conversation where the user makes a mistake and the agent corrects it.
