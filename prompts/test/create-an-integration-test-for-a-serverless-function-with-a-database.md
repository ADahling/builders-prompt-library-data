---
title: "Create an Integration Test for a Serverless Function with a Database"
slug: create-an-integration-test-for-a-serverless-function-with-a-database
stage: Test
category: "Testing & QA"
grade: C
score: 67
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-integration-test-for-a-serverless-function-with-a-database
---
# Create an Integration Test for a Serverless Function with a Database

Generate a comprehensive integration test suite to validate serverless function logic and database interactions in a realistic environment.

Variables: trigger_event, database_operation

## Prompt

You are a serverless developer. Your task is to create an integration test for a serverless function that interacts with a database. The serverless function is triggered by {{trigger_event}} and it {{database_operation}}.

Context:
- You need to test the integration between the serverless function and the database in a realistic environment.
- You will use a serverless testing framework that allows you to run the function locally and connect to a real or mock database.

Provide:
1. An integration test that triggers the serverless function with a sample event.
2. A setup for the database to be used in the test (e.g., a local Docker container or a cloud-based instance).
3. Assertions to verify that the data is written to or read from the database correctly.

## Tips

A prompt for serverless developers who need to test the integration of their functions with other services like databases.
