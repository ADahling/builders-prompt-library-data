---
title: "Standardizing Error Responses in an API"
slug: standardizing-error-responses-in-an-api
stage: Build
category: "API Design"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/standardizing-error-responses-in-an-api
---
# Standardizing Error Responses in an API

Design a standard API error format with status codes, usage guidelines, and JSON examples for validation, authentication, and other failures.

Variables: status, code, message, details

## Prompt

Create a standard error response structure for your API. Define the following:
- A base error response format that includes fields like {{status}}, {{code}}, {{message}}, and {{details}}.
- Specific error codes for common issues (e.g., 400 for bad requests, 404 for not found, 500 for internal server errors).
- Guidelines on how to use this structure in response to various situations, including validation errors and authentication failures.
- Provide JSON examples for different error scenarios.

## Tips

This will help ensure that your API users can handle errors in a consistent manner.
