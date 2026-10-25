---
title: "Refactor Existing JavaScript Unit Tests to Improve Readability and Maintainability"
slug: refactor-existing-javascript-unit-tests-to-improve-readability-and-maintainability
stage: Test
category: "Testing & QA"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactor-existing-javascript-unit-tests-to-improve-readability-and-maintainability
---
# Refactor Existing JavaScript Unit Tests to Improve Readability and Maintainability

Get a refactored JavaScript test file with clearer names, shared setup, specific assertions, fewer redundant cases, and a change summary.

Variables: module_name, test_framework, test_file_path

## Prompt

We have an existing suite of unit tests for our `{{module_name}}` module, written in JavaScript using `{{test_framework}}`. The tests are functional but have become difficult to read and maintain over time. I need you to refactor these tests to adhere to best practices.

**Instructions:**
1.  **Analyze Existing Tests:** Review the provided test file: `{{test_file_path}}`.
2.  **Refactoring Goals:**
    *   **Improve Descriptions:** Rewrite `describe` and `it` block descriptions to be more descriptive and follow a consistent naming convention (e.g., "Given [context], when [action], then [expected result]").
    *   **DRY Principle:** Identify and refactor repetitive code into helper functions or `beforeEach`/`afterEach` hooks.
    *   **Clearer Assertions:** Replace ambiguous assertions with more specific and readable ones. Add comments to explain complex assertions.
    *   **Remove Redundancy:** Eliminate redundant or overlapping test cases.
3.  **Output Format:** Provide the refactored test file as a single code block. Include a brief summary of the changes made and the rationale behind them.
