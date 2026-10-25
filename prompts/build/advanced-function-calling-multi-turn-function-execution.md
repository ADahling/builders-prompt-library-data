---
title: "Advanced Function Calling: Multi-turn Function Execution"
slug: advanced-function-calling-multi-turn-function-execution
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-function-calling-multi-turn-function-execution
---
# Advanced Function Calling: Multi-turn Function Execution

Implement a multi-turn OpenAI function calling workflow in Python to orchestrate sequential tool orchestration and state management.

## Prompt

You are building a complex AI assistant that needs to perform a series of actions to fulfill a user's request. This requires a multi-turn conversation where the model first calls a function, gets the result, and then decides on the next step, which might be another function call or a final answer to the user.

Your task is to write a Python script using the OpenAI API that demonstrates a two-step function calling process.

**Scenario:**
The user wants to know the weather in a city but provides the city name in a different language.
- **User:** "What's the weather in 'Firenze'?"

**Workflow:**
1.  **First Call:** The model doesn't know where 'Firenze' is. It should call a `translate_city_name` function to translate it to English.
2.  **Execution:** Your script executes this function, which returns "Florence".
3.  **Second Call:** Your script sends the conversation history, including the function's output, back to the model. The model now knows the city is Florence and should call the `get_weather` function.
4.  **Final Execution:** Your script executes `get_weather(location="Florence")` and gets the final answer to show the user.

**Technical Requirements:**
- Use the 'openai' Python library.
- Define two functions in your script: `translate_city_name(city: str)` (returns a hardcoded "Florence") and `get_weather(location: str)` (returns a hardcoded weather report for Florence).
- Define the schemas for both functions as tools for the OpenAI API.
- The script must manage the conversation history (`messages` list) correctly, appending the user query, the model's first function call request, your function call result, the model's second function call request, and your second function call result.
- The script should print the key steps to the console (e.g., "Calling function: translate_city_name", "Calling function: get_weather").
- Finally, after the second function call, send the result back to the model one last time to get a natural language response to print to the user.

**Output Format:**
A complete, executable Python script that implements this multi-turn function calling logic.
