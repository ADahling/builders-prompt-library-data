---
title: "Create a Prompt for Generating Unit Tests with a High Level of Coverage"
slug: create-a-prompt-for-generating-unit-tests-with-a-high-level-of-coverage
stage: Idea
category: "Prompt Engineering"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-prompt-for-generating-unit-tests-with-a-high-level-of-coverage
---
# Create a Prompt for Generating Unit Tests with a High Level of Coverage

Generate comprehensive unit tests across languages and frameworks to achieve maximum code coverage through positive, negative, and edge cases.

Variables: language, testing_framework

## Prompt

You are a software developer who is a strong advocate for test-driven development (TDD). Your task is to create a prompt that instructs an AI to generate a suite of unit tests for a given {{language}} function. The goal is to achieve a high level of code coverage.

The prompt should instruct the AI to:

1.  **Understand the Function**: Analyze the provided function and understand its purpose, inputs, and outputs.
2.  **Identify Test Cases**: Identify a comprehensive set of test cases, including positive, negative, and edge cases.
3.  **Generate Unit Tests**: For each test case, generate a unit test using the {{testing_framework}} framework.
4.  **Include Assertions**: Each unit test should include clear and specific assertions to verify the function's behavior.
5.  **Aim for High Coverage**: The generated tests should aim for at least 90% code coverage.

The user will provide the function to be tested.

## Tips

This prompt helps developers generate a comprehensive suite of unit tests, which is essential for building robust and reliable software.
