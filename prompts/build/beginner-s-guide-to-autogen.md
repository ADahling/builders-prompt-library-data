---
title: "Beginner's Guide to AutoGen"
slug: beginner-s-guide-to-autogen
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/beginner-s-guide-to-autogen
---
# Beginner's Guide to AutoGen

Get a beginner AutoGen tutorial in Markdown with core agent concepts and a runnable Python example of two agents having a conversation.

Variables: country

## Prompt

Create a beginner-friendly tutorial on Microsoft's AutoGen framework. The goal is to explain its core concepts and provide a simple "Hello, World" example.

**Tutorial Content:**

1.  **What is AutoGen?**
    *   Explain AutoGen as a framework for building applications with multiple, conversational AI agents.
    *   Emphasize its strength in creating teams of agents that can collaborate to solve problems.
2.  **Core Concepts:**
    *   **`ConversableAgent`:** The base class for all agents in AutoGen. They can send and receive messages.
    *   **`UserProxyAgent`:** A special type of agent that can act on behalf of a human user. Crucially, it can also be configured to execute code.
    *   **`AssistantAgent`:** The standard AI agent that uses an LLM to generate responses.
3.  **The Simplest Conversation: Two Agents Talking:**
    *   Show how to set up a `UserProxyAgent` and an `AssistantAgent`.
    *   Demonstrate how to use `user_proxy.initiate_chat()` to start a conversation between them.
4.  **A Simple Code Example:**
    *   Provide a complete, runnable Python script.
    *   The user proxy should ask the assistant a question like, "What is the largest city in {{country}}?"
    *   The assistant should respond, and the conversation should end.

**Output Format:**

A Markdown file containing the tutorial. The code should be simple and well-commented to illustrate the basic principles of AutoGen.
