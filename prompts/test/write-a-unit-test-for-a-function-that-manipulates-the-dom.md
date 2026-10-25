---
title: "Write a Unit Test for a Function that Manipulates the DOM"
slug: write-a-unit-test-for-a-function-that-manipulates-the-dom
stage: Test
category: "Testing & QA"
grade: B
score: 75
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-unit-test-for-a-function-that-manipulates-the-dom
---
# Write a Unit Test for a Function that Manipulates the DOM

Generate comprehensive unit tests using virtual DOM libraries to verify specific DOM manipulations and handle invalid input scenarios.

Variables: dom_manipulation, testing_library

## Prompt

You are a frontend developer. Your task is to write a unit test for a function that manipulates the DOM. The function takes a DOM element as input and {{dom_manipulation}}.

Context:
- You need to use a testing library that provides a virtual DOM, such as {{testing_library}}, to test the function without a real browser.
- You will create a mock DOM element and pass it to the function.

Provide:
1. A unit test that calls the function with a mock DOM element.
2. Assertions to verify that the DOM element is manipulated correctly.
3. A test case to handle the scenario where the input is not a valid DOM element.

## Tips

A beginner-friendly prompt for frontend developers to learn how to test DOM manipulation code.
