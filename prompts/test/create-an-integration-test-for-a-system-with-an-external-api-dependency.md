---
title: "Create an Integration Test for a System with an External API Dependency"
slug: create-an-integration-test-for-a-system-with-an-external-api-dependency
stage: Test
category: "Testing & QA"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-integration-test-for-a-system-with-an-external-api-dependency
---
# Create an Integration Test for a System with an External API Dependency

Generate an automated integration test with mocked external API responses to verify system behavior without relying on third-party uptime.

Variables: api_functionality

## Prompt

You are a software engineer. Your task is to create an integration test for a system that has a dependency on an external API. The system calls the external API to {{api_functionality}}.

Context:
- You need to test the integration between your system and the external API without making real calls to the API in your test environment.
- You should use a mocking or stubbing technique to simulate the external API.

Provide:
1. An integration test that calls the system and triggers the interaction with the external API.
2. A mock or stub of the external API that returns a predefined response.
3. Assertions to verify that the system behaves correctly based on the response from the mock API.

## Tips

A prompt for engineers who need to test systems with external dependencies, which is a common scenario in modern software development.
