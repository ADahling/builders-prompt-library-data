---
title: "Generate integration tests for a microservice"
slug: generate-integration-tests-for-a-microservice
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-integration-tests-for-a-microservice
---
# Generate integration tests for a microservice

Generate comprehensive integration tests for user creation and retrieval endpoints to validate schema compliance and error handling across specific languages.

Variables: user_id, framework, language

## Prompt

You are an AI coding assistant. Generate a suite of integration tests for a microservice that has two endpoints: `POST /users` and `GET /users/{{user_id}}`.

Use the `{{framework}}` framework for `{{language}}`.

The tests should cover:
1. Creating a new user and then retrieving it.
2. Trying to retrieve a user that does not exist.
3. Validating the response schemas.

## Tips

A practical prompt for automating integration test generation.
