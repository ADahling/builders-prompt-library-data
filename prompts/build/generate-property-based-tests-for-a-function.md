---
title: "Generate property-based tests for a function"
slug: generate-property-based-tests-for-a-function
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-property-based-tests-for-a-function
---
# Generate property-based tests for a function

Generate property-based tests using your preferred framework to verify the integrity, order, and consistency of integer sorting functions.

Variables: framework, language

## Prompt

You are an AI coding assistant. Generate a suite of property-based tests for a function that sorts a list of integers.

Use the `{{framework}}` framework for `{{language}}`.

The properties to test should include:
1. The output list has the same length as the input list.
2. The output list is sorted in ascending order.
3. The output list contains the same elements as the input list.

## Tips

A practical prompt for automating property-based test generation.
