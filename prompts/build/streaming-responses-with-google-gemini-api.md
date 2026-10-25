---
title: "Streaming Responses with Google Gemini API"
slug: streaming-responses-with-google-gemini-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/streaming-responses-with-google-gemini-api
---
# Streaming Responses with Google Gemini API

Implement a Python script using the Google Gemini API to stream real-time text chunks for an engaging, low-latency user experience.

## Prompt

As a developer creating an interactive educational tool, you want to use the Google Gemini API to generate explanations that appear on the screen in real-time, which enhances user engagement.

Your task is to write a Python script that sends a prompt to the Gemini API and streams the response. The script will print the generated content to the console chunk by chunk as it is received.

**Scenario:**
Ask the Gemini model to "Explain the concept of photosynthesis in simple terms, as if you were talking to a 10-year-old."

**Technical Requirements:**
- Use the 'google-generativeai' Python library and the Gemini 3 Flash model.
- The API call to `model.generate_content` must include the parameter `stream=True`.
- The script needs to loop through the streaming response object.
- For each chunk received, it should access the `text` attribute and print it to the console without a newline character to simulate a continuous flow of text.
- Ensure the output is flushed to the console immediately after printing each chunk.

**Output Format:**
A single, executable Python script that demonstrates handling a streaming response from the Gemini API.
