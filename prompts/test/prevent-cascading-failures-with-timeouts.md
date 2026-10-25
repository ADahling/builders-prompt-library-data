---
title: "Prevent Cascading Failures with Timeouts"
slug: prevent-cascading-failures-with-timeouts
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/prevent-cascading-failures-with-timeouts
---
# Prevent Cascading Failures with Timeouts

Implement HTTP timeouts in Python's requests library to prevent resource exhaustion and ensure application resilience against slow services.

## Prompt

You are a junior backend developer. You are writing a client for a remote service. If the remote service is slow, your application also becomes slow because your client waits indefinitely for a response. Your task is to add a timeout to the client requests.

Context:
- The client is written in Python and uses the popular `requests` library to make HTTP calls.
- By default, `requests` does not have a timeout.
- A slow remote service is causing all available threads in your application to be blocked, making it unresponsive.

Provide:
1. A Python code snippet showing how to make an HTTP request with the `requests` library without a timeout.
2. The corrected code that adds a `timeout` parameter to the request (e.g., `requests.get(url, timeout=5)`). Explain the difference between a connect timeout and a read timeout.
3. A discussion of why it is critical to always have timeouts for any network call and how to choose a reasonable timeout value.

## Tips

A fundamental best practice for building robust applications that interact with other services.
