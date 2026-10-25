---
title: "Streaming Responses with OpenAI API for Real-time Applications"
slug: streaming-responses-with-openai-api-for-real-time-applications
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/streaming-responses-with-openai-api-for-real-time-applications
---
# Streaming Responses with OpenAI API for Real-time Applications

Implement real-time token streaming using the OpenAI Python library to display AI-generated text incrementally for responsive applications.

## Prompt

You are developing a web application that features a real-time AI writing assistant. To provide a responsive user experience, you need to stream the AI's response token by token, similar to how ChatGPT types out its answers.

Your task is to create a Python script that makes a request to the OpenAI Chat Completions API with streaming enabled. The script should process the stream and print each chunk of content to the console as it is received.

**Scenario:**
Request the AI to write a short, 3-sentence paragraph on the topic: "The importance of unit testing in software development."

**Technical Requirements:**
- Use the 'openai' Python library and a fast chat model (e.g., 'gpt-5').
- In the `client.chat.completions.create` call, you must set the parameter `stream=True`.
- The script must iterate through the response stream.
- For each chunk in the stream, it should check if there is content available and, if so, print it to the console immediately.
- Use `end=''` and `flush=True` in your print statement to ensure the tokens appear on the same line and are displayed in real-time.
- The script should gracefully handle the end of the stream.

**Output Format:**
A single, executable Python script that demonstrates how to handle a streaming response from the OpenAI API.
