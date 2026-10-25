---
title: "Write an API Test for a RESTful Endpoint"
slug: write-an-api-test-for-a-restful-endpoint
stage: Test
category: "Testing & QA"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-an-api-test-for-a-restful-endpoint
---
# Write an API Test for a RESTful Endpoint

Generate comprehensive API tests with valid and invalid cases to ensure RESTful endpoint functionality, security, and error handling.

Variables: endpoint_functionality, endpoint_url, request_method, backend_framework, authentication_method

## Prompt

You are a backend developer. Your task is to write an API test for a RESTful endpoint that {{endpoint_functionality}}. The endpoint is available at {{endpoint_url}} and accepts {{request_method}} requests.

Context:
- The API is built with {{backend_framework}}.
- The endpoint requires {{authentication_method}} for access.

Provide:
1. An API test that sends a request to the endpoint with valid data.
2. Assertions to verify the status code, headers, and body of the response.
3. A test case for an invalid request to ensure proper error handling.

## Tips

A fundamental prompt for backend developers to learn how to test RESTful APIs.
