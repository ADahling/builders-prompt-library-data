---
title: "Agent with Short-Term and Long-Term Memory"
slug: agent-with-short-term-and-long-term-memory
stage: Build
category: "AI Agent Development"
grade: C
score: 62
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agent-with-short-term-and-long-term-memory
---
# Agent with Short-Term and Long-Term Memory

Design a personal assistant agent with recent conversation memory and vector-stored session summaries to recall details across conversations.

## Prompt

Develop an AI agent that possesses both short-term and long-term memory. The agent should be able to hold a conversation, remember key details within that conversation (short-term), and also recall information from previous, separate conversations (long-term).

**Memory System Design:**

1.  **Short-Term Memory:**
    *   Use `ConversationBufferWindowMemory` from LangChain to keep track of the last `k` interactions in the current conversation.
    *   Set `k` to a reasonable number, like 5.
2.  **Long-Term Memory:**
    *   Use a vector store (e.g., FAISS or Chroma) for long-term storage.
    *   After each conversation, summarize the key information and store it as a document in the vector store.
3.  **Memory Retrieval:**
    *   Before generating a response, the agent should query the long-term memory for any relevant context from past conversations based on the current user input.
    *   This retrieved context should be combined with the short-term memory to provide a comprehensive context for the LLM.

**Agent's Task:**

The agent will act as a personal assistant. The user can tell it about their preferences, tasks, and other personal information. The agent should be able to recall this information in later conversations.

**Example Scenario:**

*   **Conversation 1:**
    *   **User:** "I'm allergic to peanuts."
    *   **Agent:** "Got it. I'll remember that."
*   **(Agent summarizes and stores 'User is allergic to peanuts' in long-term memory)**
*   **Conversation 2 (a day later):**
    *   **User:** "Can you suggest a recipe for dinner?"
    *   **Agent:** "Of course. Just to be safe, I'll make sure to suggest recipes that do not contain peanuts, since you mentioned you have an allergy."

**Technical Implementation:**

*   Use Python, LangChain, and a vector store library.
*   Create a custom agent loop that manages the two memory systems and the interaction with the LLM.
