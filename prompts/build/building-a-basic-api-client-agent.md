---
title: "Building a Basic API Client Agent"
slug: building-a-basic-api-client-agent
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-basic-api-client-agent
---
# Building a Basic API Client Agent

Get a Python script for a LangChain ReAct agent that queries JSONPlaceholder users to demonstrate tool use with a public API.

Variables: user_name

## Prompt

Create a simple AI agent that can interact with a public, no-auth API to retrieve information. This is a fundamental example of tool use.

**The API:**

Use the JSONPlaceholder API, which is a free fake REST API. We will use the `/users` endpoint.

**The Tool:**

1.  Create a Python function `get_users()` that makes an HTTP GET request to `https://jsonplaceholder.typicode.com/users`.
2.  The function should return the JSON response (a list of user dictionaries).
3.  Wrap this function in a LangChain `Tool` with a clear name and description.

**The Agent:**

1.  Initialize a simple ReAct agent.
2.  Provide the `get_users` tool to the agent.
3.  Ask the agent a question that requires it to use the tool, such as: "How many users are in the system?" or "What is the email address of the user named '{{user_name}}'?"

**Your Task:**

Write a Python script that defines the tool, creates the agent, and runs it to answer a question using the live API.

**Output:**

A complete, runnable Python script.
