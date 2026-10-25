---
title: "Write a Unit Test for a Function that Uses a Generator"
slug: write-a-unit-test-for-a-function-that-uses-a-generator
stage: Test
category: "Testing & QA"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-unit-test-for-a-function-that-uses-a-generator
---
# Write a Unit Test for a Function that Uses a Generator

Generate Python unit tests that validate generator outputs by converting yields to lists and asserting sequence accuracy, including empty cases.

Variables: function_name, value_type

## Prompt

You are a Python developer. Your task is to write a unit test for a function that uses a generator to produce a sequence of values. The generator function is called {{function_name}} and it yields {{value_type}}.

Context:
- You need to test that the generator function yields the correct sequence of values.
- You will iterate over the generator and check each value.

Provide:
1. A unit test that calls the generator function and converts the generator to a list.
2. Assertions to verify that the list of values is correct.
3. A test case to handle the scenario where the generator is empty.

## Tips

A prompt for developers to learn how to test generator functions, which are a powerful feature in some programming languages.
