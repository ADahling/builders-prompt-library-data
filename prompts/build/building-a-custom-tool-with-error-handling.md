---
title: "Building a Custom Tool with Error Handling"
slug: building-a-custom-tool-with-error-handling
stage: Build
category: "AI Agent Development"
grade: A
score: 84
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-custom-tool-with-error-handling
---
# Building a Custom Tool with Error Handling

Get a Python script demonstrating a LangChain tool that returns helpful errors for missing users, with successful and failed agent calls.

Variables: user_id

## Prompt

Create a robust custom tool for a LangChain agent that includes its own error handling. The tool should not crash the agent but instead return a helpful error message to the LLM.

**The Tool:**

A tool called `get_user_data(user_id: int)` that simulates fetching data from a database.

**The Logic:**

1.  The tool function should have a `try...except` block.
2.  Inside the `try` block, it attempts to access a dictionary (simulating the database). `db = {1: 'Alice', 2: 'Bob'}`.
3.  If the `user_id` exists, it returns the user's data.
4.  If the `user_id` does not exist (which will raise a `KeyError`), the `except` block should catch the error.
5.  Instead of re-raising the error, the `except` block should return a descriptive string: "Error: User with ID {{user_id}} not found."

**Agent Setup:**

*   Create a ReAct agent and give it this tool.
*   Ask the agent to find data for a user that exists (e.g., user 1) and a user that does not exist (e.g., user 99).

**Expected Behavior:**

When asked for user 99, the agent should not crash. It should receive the error message from the tool and then respond to the user, "I could not find any data for user 99."

**Output:**

A Python script that defines the robust tool and demonstrates the agent handling both a successful and a failed tool call gracefully.
