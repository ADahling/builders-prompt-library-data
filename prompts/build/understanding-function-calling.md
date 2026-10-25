---
title: "Understanding Function Calling"
slug: understanding-function-calling
stage: Build
category: "AI Agent Development"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/understanding-function-calling
---
# Understanding Function Calling

Get a junior developer guide to LLM function calling, explaining structured tool requests and the application's execution loop.

## Prompt

Create an educational guide for junior developers explaining the concept of "function calling" in large language models (LLMs).

**Guide Structure:**

1.  **The Problem:**
    *   Start by explaining the limitations of LLMs. They are great at text, but they can't perform real-world actions (like sending an email, checking a database, or getting live data).
2.  **What is Function Calling?**
    *   Explain function calling as a way for an LLM to ask for a tool to be used. The LLM doesn't *execute* the function itself; it generates a structured request (usually JSON) asking the application to run a specific function with specific arguments.
3.  **How it Works (The "Loop"):**
    *   **Step 1: User Prompt:** The user asks a question that requires external data or action (e.g., "What's the weather in London?").
    *   **Step 2: LLM Decides:** The application sends the user's prompt and a list of available functions to the LLM. The LLM decides that it needs to call the `get_weather` function with the argument `city="London"`.
    *   **Step 3: LLM Responds with JSON:** The LLM's response is not a sentence, but a JSON object like `{"function": "get_weather", "arguments": {"city": "London"}}`.
    *   **Step 4: Application Executes:** The application code parses this JSON, calls its own `get_weather("London")` function, and gets the result (e.g., "15°C and cloudy").
    *   **Step 5: Application Sends Result to LLM:** The application sends this result back to the LLM.
    *   **Step 6: LLM Generates Final Answer:** The LLM now has the information it needs and generates a natural language response for the user: "The weather in London is 15°C and cloudy."
4.  **Simple Code Snippet:**
    *   Provide a conceptual Python code snippet showing how to make a call to the OpenAI API with a function definition.

**Output Format:**

A clear and concise explanation in a Markdown file. Use simple language and analogies to make the concept easy to grasp.
