---
title: "AI Safety: Using the OpenAI Content Moderation API"
slug: ai-safety-using-the-openai-content-moderation-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/ai-safety-using-the-openai-content-moderation-api
---
# AI Safety: Using the OpenAI Content Moderation API

Develop a Python script using the OpenAI Moderation API to programmatically detect and report policy violations in user-generated text.

## Prompt

You are the administrator of an online forum and want to automatically flag user-generated content that violates your community guidelines. You will use the OpenAI Moderation API to check text for harmful content before it gets published.

Your task is to write a Python script that sends a piece of text to the Moderation API and interprets the results.

**Input Text to Check:**
"This is a test post. I'm going to ignore the rules and just say whatever I want. This platform is terrible anyway."

**Technical Requirements:**
- Use the 'openai' Python library.
- The script should make a call to `client.moderations.create()` with the input text.
- The API response contains a 'results' array. Your script should parse this response.
- For each category in the moderation results (e.g., 'hate', 'violence', 'self-harm'), print the category name and whether it was flagged ('True' or 'False').
- Finally, the script should check the overall 'flagged' status for the entire input and print a summary message, such as "Content has been flagged." or "Content seems safe."

**Output Format:**
A complete Python script that analyzes a piece of text and prints a summary of the moderation results.
