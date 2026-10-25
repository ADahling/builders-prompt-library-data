---
title: "Anthropic Claude API: Conversational Chat for a Technical Tutor"
slug: anthropic-claude-api-conversational-chat-for-a-technical-tutor
stage: Build
category: "LLM & AI Integration"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/anthropic-claude-api-conversational-chat-for-a-technical-tutor
---
# Anthropic Claude API: Conversational Chat for a Technical Tutor

Develop a Python script using the Anthropic SDK to simulate a multi-turn Socratic tutoring session about Python dictionaries.

## Prompt

Act as a developer building an AI-powered technical tutor for Python programming.

Your task is to create a Python script that uses the Anthropic Claude Opus 4.8 model for a multi-turn conversation. The tutor's persona is that of a patient and knowledgeable expert who guides users to discover solutions themselves rather than giving direct answers.

**Scenario:**
A user is struggling to understand Python dictionaries.

**Conversation History:**
1.  **User:** "I don't get Python dictionaries. What are they?"
2.  **Assistant:** (Your script should generate a response to this first user message, explaining dictionaries with an analogy.)
3.  **User:** "Okay, so it's like a list but with names for each item? How do I get a value out of it?"

**Technical Requirements:**
- Use the 'anthropic' Python SDK and the 'claude-opus-4-8-2026' model.
- Your script must model the conversation history provided above.
- The prompt to Claude for the final turn must include the previous user and assistant messages to provide context.
- The final instruction to Claude should be to answer the user's last question ("How do I get a value out of it?") in a way that encourages the user to think, perhaps by providing a small code snippet and asking what they think it does.
- Print only the assistant's final response to the console.

**Output Format:**
A complete Python script that simulates the conversation and prints the final AI-generated response.
