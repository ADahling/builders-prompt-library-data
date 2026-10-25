---
title: "Google Gemini API: Function Calling for a Weather Chatbot"
slug: google-gemini-api-function-calling-for-a-weather-chatbot
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/google-gemini-api-function-calling-for-a-weather-chatbot
---
# Google Gemini API: Function Calling for a Weather Chatbot

Implement an executable Python script using the Gemini API to demonstrate how the model triggers specialized tool calls from natural language.

## Prompt

Act as an AI developer building a smart chatbot that can provide real-time weather information by calling an external function.

Your task is to create a Python script using the Google Gemini API's function calling feature. The chatbot will understand a user's request for the weather, and instead of answering directly, it will generate a call to a function you've defined.

**Scenario:**
The user asks: "What's the weather like in London?"

**Function Definition:**
You must define a Python function `get_weather(location: str)`. For this example, this function will not make a real API call but will return a hardcoded JSON string: `{"location": "London", "temperature": "15°C", "condition": "Cloudy"}`.

**Technical Requirements:**
- Use the 'google-generativeai' library and the Gemini 3 Pro model.
- Define the `get_weather` function and its schema (description, parameters, types) for the Gemini API.
- The tool schema must be passed to the model in the `tools` parameter during the initial `generate_content` call.
- The script must first send the user's question to the model.
- It should then check if the model's response contains a function call.
- If a function call is present, the script must print the name of the function to be called and its arguments.
- You do not need to execute the function and send the result back to the model for this exercise. The goal is to demonstrate the model's ability to generate the correct function call.

**Output Format:**
A complete Python script that prints the function name and arguments identified by the Gemini model.
