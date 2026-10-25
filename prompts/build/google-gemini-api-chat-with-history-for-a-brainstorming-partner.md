---
title: "Google Gemini API: Chat with History for a Brainstorming Partner"
slug: google-gemini-api-chat-with-history-for-a-brainstorming-partner
stage: Build
category: "LLM & AI Integration"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/google-gemini-api-chat-with-history-for-a-brainstorming-partner
---
# Google Gemini API: Chat with History for a Brainstorming Partner

Implement a Python script using the Gemini API to manage stateful chat history for brainstorming innovative mobile app features.

## Prompt

Act as a developer creating a brainstorming assistant using the Google Gemini API.

Your task is to build a Python script that maintains a conversation history to facilitate a creative brainstorming session. The assistant should help a user flesh out an idea for a new mobile app.

**Scenario:**
The user wants to build an app for local community gardening.

**Conversation Flow:**
1.  **User:** "I have an idea for a mobile app to help local gardeners connect and share produce. What are some potential features?"
2.  **Assistant:** (Generates a list of initial feature ideas: e.g., plant-swapping marketplace, gardening Q&A forum, local event calendar).
3.  **User:** "I like the marketplace idea. How could we make that feature really unique?"

**Technical Requirements:**
- Use the 'google-generativeai' library and the Gemini 3 model.
- The script must initialize a chat session using `model.start_chat(history=[...])`.
- The history must be populated with the first user message and a plausible assistant response.
- The script should then send the user's second message ("I like the marketplace idea...") to the chat session.
- The final instruction to the model should be to brainstorm unique, innovative ideas for the marketplace feature, building upon the existing conversation context.
- Print the assistant's final, creative response to the console.

**Output Format:**
A complete Python script that demonstrates the multi-turn chat capability.
