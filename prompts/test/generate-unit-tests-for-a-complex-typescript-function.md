---
title: "Generate Unit Tests for a Complex TypeScript Function"
slug: generate-unit-tests-for-a-complex-typescript-function
stage: Test
category: "Testing & QA"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-unit-tests-for-a-complex-typescript-function
---
# Generate Unit Tests for a Complex TypeScript Function

Generate a robust TypeScript unit test suite with full edge case coverage and dependency mocking for critical project functions.

Variables: function_code, project_name, tech_stack, test_framework, mocking_library, assertion_library, file_name

## Prompt

As a senior software engineer, I need you to generate a comprehensive suite of unit tests for the following TypeScript function: `{{function_code}}`.

The function is part of a critical module in our `{{project_name}}` project, which uses the `{{tech_stack}}` stack. Your primary goal is to ensure maximum test coverage, including all edge cases, error conditions, and potential failure points.

**Instructions:**
1.  **Test Framework:** Use `{{test_framework}}` (e.g., Jest, Mocha) for the test suite.
2.  **Mocking:** Where necessary, use `{{mocking_library}}` (e.g., jest.fn(), Sinon.js) to mock external dependencies, API calls, or database interactions.
3.  **Assertions:** Employ a wide range of assertions from `{{assertion_library}}` (e.g., Chai, expect) to validate the function's behavior, including deep equality checks for objects and arrays.
4.  **Test Cases:**
    *   **Happy Path:** At least three test cases for valid inputs and expected outputs.
    *   **Edge Cases:** Test with empty strings, null values, undefined inputs, and zero values.
    *   **Error Handling:** Verify that the function correctly throws specific, documented errors for invalid inputs or exceptional circumstances.
    *   **Performance:** (Optional) Include a basic performance test to ensure the function executes within an acceptable time frame.
5.  **Output Format:** Provide the complete test file as a single code block, ready to be saved as `{{file_name}}.test.ts`. The code must be well-documented, with clear descriptions for each `describe` and `it` block.
