---
title: "Basic Agent with No Tools"
slug: basic-agent-with-no-tools
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/basic-agent-with-no-tools
---
# Basic Agent with No Tools

Get a runnable Python script for a tool-free LangChain agent that answers general knowledge questions, as an introduction to agent basics.

Variables: question

## Prompt

Create the simplest possible AI agent: one that has no tools and relies solely on the knowledge of its underlying LLM to answer questions. This is a foundational exercise to understand the core components of an agent.

**Components:**

1.  **LLM:** An LLM from LangChain, such as `OpenAI` or `ChatOpenAI`.
2.  **Prompt:** A simple prompt template that takes the user's input.
3.  **Chain:** A `LLMChain` that combines the LLM and the prompt.

**Functionality:**

The agent will be able to answer general knowledge questions that are within the LLM's training data. It will not be able to answer questions about current events or access any external information.

**Implementation Steps:**

1.  Set up your Python environment with `langchain` and `openai`.
2.  Initialize your chosen LLM.
3.  Create a `PromptTemplate` that includes a placeholder for the user's `{{question}}`.
4.  Create an `LLMChain` with the LLM and the prompt.
5.  Write a simple loop that takes user input and calls the chain's `run` method.
6.  Print the output.

**Example Questions:**

*   "What is the capital of Japan?"
*   "Explain the theory of relativity in simple terms."

**Output:**

A complete, runnable Python script that demonstrates this basic agent.
