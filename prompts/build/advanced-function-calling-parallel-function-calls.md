---
title: "Advanced Function Calling: Parallel Function Calls"
slug: advanced-function-calling-parallel-function-calls
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-function-calling-parallel-function-calls
---
# Advanced Function Calling: Parallel Function Calls

Implement parallel tool calling in Python to simultaneously fetch stock data and news headlines using the OpenAI Chat Completions API.

## Prompt

You are building a financial dashboard AI that needs to fetch information from multiple sources at once to answer a user's query efficiently. You will use the parallel function calling feature available in newer LLM APIs (like OpenAI's).

Your task is to write a Python script that demonstrates how an LLM can request multiple function calls in a single turn.

**Scenario:**
- **User Query:** "What's the current stock price of AAPL and what's the latest news about Google?"
- **Functions:** You have two functions defined:
    -   `get_stock_price(symbol: str)`
    -   `get_latest_news(company_name: str)`

**Technical Requirements:**
- Use the 'openai' Python library and a model that supports parallel function calling (e.g., `gpt-5`).
- Define the two Python functions. For this example, they can return hardcoded data (e.g., `get_stock_price` returns 150.0, `get_latest_news` returns "Google launches new AI model.").
- Define the schemas for both functions and pass them in the `tools` parameter of the API call.
- Make a single call to the Chat Completions API with the user's query.
- The model's response should contain *two* separate tool calls in the `tool_calls` list.
- Your script must iterate through the `tool_calls` list.
- For each tool call, identify the function name and its arguments.
- Execute the corresponding local function.
- Print the results of both function calls to the console.

**Output Format:**
A complete, executable Python script that shows the model requesting two functions at once and the script executing both.
