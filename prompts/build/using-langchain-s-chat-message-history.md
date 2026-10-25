---
title: "Using LangChain's Chat Message History"
slug: using-langchain-s-chat-message-history
stage: Build
category: "AI Agent Development"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/using-langchain-s-chat-message-history
---
# Using LangChain's Chat Message History

Get a Python script to pre-populate LangChain chat history, use it in a conversation chain, and inspect updated messages for agent memory.

## Prompt

Demonstrate how to manage and manipulate a conversation's history using LangChain's `ChatMessageHistory` objects. This gives you fine-grained control over an agent's memory.

**The Scenario:**

You want to build a conversational agent but need to be able to manually add messages to its history or summarize it periodically to save tokens.

**Your Task:**

1.  **Initialize History:** Create an instance of `ChatMessageHistory`.
2.  **Add Messages:**
    *   Show how to add user messages using `history.add_user_message()`.
    *   Show how to add AI messages using `history.add_ai_message()`.
3.  **Integrate with a Chain:**
    *   Create a `ConversationChain`.
    *   Instead of using a standard memory object, pass your `ChatMessageHistory` instance to a `ConversationBufferMemory` object using the `chat_memory` parameter.
4.  **Run and Verify:**
    *   Run the chain with a new message. The chain should use the history you manually created as its context.
    *   After the run, inspect the `history.messages` object to see that the new turn has been added.

**Output:**

A Python script that shows how to create a history object, pre-populate it with messages, use it in a conversation, and then inspect the updated history.
