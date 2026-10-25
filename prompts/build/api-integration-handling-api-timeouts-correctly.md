---
title: "API Integration: Handling API Timeouts Correctly"
slug: api-integration-handling-api-timeouts-correctly
stage: Build
category: "LLM & AI Integration"
grade: C
score: 64
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-integration-handling-api-timeouts-correctly
---
# API Integration: Handling API Timeouts Correctly

Implement robust API request handling in Python by setting timeouts and managing exceptions to prevent application hangs during slow responses.

## Prompt

You are integrating with a third-party API that is occasionally slow to respond. If the API takes too long, your application hangs, providing a poor user experience. You need to implement a timeout on your API requests.

Your task is to write a Python script using the 'requests' library that demonstrates how to set a timeout and handle the `Timeout` exception.

**Scenario:**
- You will make a request to `http://httpbin.org/delay/5
