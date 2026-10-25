---
title: "OpenAI API: Function Calling for Database Queries"
slug: openai-api-function-calling-for-database-queries
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openai-api-function-calling-for-database-queries
---
# OpenAI API: Function Calling for Database Queries

Generate a Python script that uses OpenAI function calling to translate natural language user requests into structured database query arguments.

## Prompt

As a senior backend engineer, you are designing an AI-powered natural language interface for your company's database. Users should be able to ask questions in plain English, which the AI will translate into structured database queries.

Your task is to write a Python script that uses the OpenAI API's function calling feature to convert a user's request into a structured query object.

**User Request:**
"Show me all active users from Canada who signed up in the last 30 days."

**Function and Schema:**
You need to define a function schema for a tool named `query_database`. This tool should accept the following parameters:
- `status` (string, enum: ["active", "inactive", "pending"])
- `country_code` (string, ISO 3166-1 alpha-2 format)
- `days_since_signup` (integer)

**Technical Requirements:**
- Use the 'openai' Python library and a model that supports function calling (e.g., 'gpt-5').
- Define the tool schema for `query_database` in the format required by the OpenAI API.
- The script should send the user's natural language request to the Chat Completions API, along with the tool definition.
- The model is expected to respond with a request to call the `query_database` function with the appropriate arguments extracted from the user's query.
- Your script must parse the model's response, extract the function name and arguments, and print them to the console in a clean, readable format.

**Output Format:**
A complete Python script that demonstrates this natural language to structured query conversion.
