---
title: "Creating a Simple Chatbot with Memory"
slug: creating-a-simple-chatbot-with-memory
stage: Build
category: "AI Agent Development"
grade: B
score: 79
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-simple-chatbot-with-memory
---
# Creating a Simple Chatbot with Memory

Get a Python script for a LangChain chatbot that stores conversation history in buffer memory and responds through an interactive input loop.

## Prompt

Build a basic chatbot that can remember the context of the current conversation. This is a fundamental skill in building any conversational AI.

**The Core Component: Memory**

**Your Task:**

Use LangChain to create a simple conversational chain with memory.

1.  **LLM:** Choose a conversational model like `ChatOpenAI`.
2.  **Memory:** Use `ConversationBufferMemory`. This is the simplest memory type. It stores the entire conversation history as a string.
3.  **Prompt:** Use a `ChatPromptTemplate` that is designed for conversation. It will typically have a placeholder for the `history` and the user's `input`.
4.  **Chain:** Combine these components using `ConversationChain`.

**Implementation:**

*   Instantiate the model, memory, and prompt.
*   Create the `ConversationChain`.
*   Create a `while` loop that takes user input, passes it to the chain's `predict` method, and prints the response.

**Example Interaction to Test:**

1.  User: "My favorite color is blue."
2.  Agent: "That's a great color!"
3.  User: "What is my favorite color?"
4.  Agent: "Your favorite color is blue."

**Output:**

A complete, runnable Python script for this simple chatbot.
