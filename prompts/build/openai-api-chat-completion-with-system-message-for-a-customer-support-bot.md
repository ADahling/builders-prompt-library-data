---
title: "OpenAI API: Chat Completion with System Message for a Customer Support Bot"
slug: openai-api-chat-completion-with-system-message-for-a-customer-support-bot
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/openai-api-chat-completion-with-system-message-for-a-customer-support-bot
---
# OpenAI API: Chat Completion with System Message for a Customer Support Bot

Implement a Python script using the OpenAI API to build a specialized customer support chatbot with strict behavioral constraints and persona.

## Prompt

As a senior AI engineer, you are building a customer support chatbot for an e-commerce company called "GadgetGalaxy".

Your task is to create a Python script that uses the OpenAI Chat Completions API to power the chatbot. The chatbot's persona and constraints must be defined in a system message.

**Chatbot Persona & Rules (to be included in the system message):**
- You are "GalaxyBot", a friendly and helpful customer support assistant for GadgetGalaxy.
- Your tone should be professional yet approachable.
- You must NOT handle any requests related to refunds or personal data changes. For these, you must direct the user to contact a human agent at support@gadgetgalaxy.com.
- You can answer questions about order status, product details, and shipping information.
- You should ask clarifying questions if the user's query is ambiguous.

**Technical Requirements:**
- Use the 'openai' Python library and a modern chat model (e.g., 'gpt-5').
- The script should simulate a conversation history, where the user asks a question about their order status.
- The system message must clearly define the chatbot's persona and rules as described above.
- The user's message should be: "Hey, where is my order #GG12345?"
- The script should then make a call to the Chat Completions API with the system message and the user's message.
- Print the assistant's response to the console.

**Output Format:**
A complete, executable Python script.
