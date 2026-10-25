---
title: "API Integration: Implementing Exponential Backoff"
slug: api-integration-implementing-exponential-backoff
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-integration-implementing-exponential-backoff
---
# API Integration: Implementing Exponential Backoff

Write a Python script with a custom exponential backoff decorator and mock API call to demonstrate retries for temporary API failures.

## Prompt

When calling external APIs like OpenAI or Anthropic, rate limits (HTTP 429) or temporary server errors (HTTP 500/502) are common. A robust application must handle these gracefully by retrying the request with increasing delays.

Your task is to write a Python script that implements a custom exponential backoff decorator and applies it to a mock API call.

**Technical Requirements:**
- Do not use external retry libraries like `tenacity` or `backoff`; write the logic from scratch to demonstrate understanding.
- Create a Python decorator named `@exponential_backoff`.
- The decorator should accept parameters: `max_retries` (default 3) and `base_delay` (default 1 second).
- Inside the decorator, use a `try...except` block within a loop.
- If an exception occurs, calculate the sleep time: `base_delay * (2 ** attempt_number)`.
- Use `time.sleep()` to wait, then retry.
- If `max_retries` is reached, re-raise the exception.
- Create a mock function `unreliable_api_call()` that randomly raises an exception 70% of the time and returns "Success!" 30% of the time.
- Apply your decorator to this mock function and call it, printing the results and retry attempts to the console.

**Output Format:**
A complete Python script containing the custom decorator and the mock test.
