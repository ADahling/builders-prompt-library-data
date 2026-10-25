---
title: "OpenRouter API: Unified Access to Multiple Models"
slug: openrouter-api-unified-access-to-multiple-models
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openrouter-api-unified-access-to-multiple-models
---
# OpenRouter API: Unified Access to Multiple Models

Create a Python script using the OpenAI SDK to compare responses from multiple AI models through the OpenRouter API gateway.

## Prompt

You are building an AI playground application that allows users to test their prompts against different models (e.g., OpenAI's GPT-5, Anthropic's Claude Sonnet 5, and Meta's Llama 4) without needing separate API keys for each provider. You will use OpenRouter as a unified gateway.

Your task is to write a Python script that sends the exact same prompt to two different models via the OpenRouter API and prints their responses side-by-step.

**Scenario:**
- **Prompt:** "Write a haiku about a robot learning to paint."
- **Models to Test:** `openai/gpt-5` and `anthropic/claude-sonnet-5`.

**Technical Requirements:**
- Use the 'openai' Python SDK (OpenRouter is OpenAI-compatible).
- Set the base URL to `https://openrouter.ai/api/v1`.
- Authenticate using the `OPENROUTER_API_KEY` environment variable.
- You must also include the `HTTP-Referer` and `X-Title` headers in your client initialization (as recommended by OpenRouter docs) to identify your app.
- Create a function that takes a model name and a prompt, makes the API call, and returns the response.
- Call this function twice, once for each model.
- Print the model name and its generated haiku to the console.

**Output Format:**
A complete, executable Python script demonstrating how to route requests to different models using OpenRouter.
