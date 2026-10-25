---
title: "Measure and Improve Unit Test Coverage"
slug: measure-and-improve-unit-test-coverage
stage: Test
category: "Testing & QA"
grade: B
score: 71
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/measure-and-improve-unit-test-coverage
---
# Measure and Improve Unit Test Coverage

Get a Markdown plan to measure unit test coverage, with report commands, prioritized files, missing tests, and testability recommendations.

Variables: project_name, test_runner

## Prompt

Our project, `{{project_name}}`, has a suite of unit tests, but we are unsure of their effectiveness. I need a plan to measure the current test coverage and a strategy to improve it.

**Instructions:**
1.  **Measure Coverage:**
    *   Configure our test runner (`{{test_runner}}`) to generate a test coverage report.
    *   Run the tests and analyze the report to identify uncovered lines, branches, and functions.
2.  **Improvement Strategy:**
    *   **Prioritize:** Identify critical modules or files with low coverage that need immediate attention.
    *   **Write Missing Tests:** For the prioritized files, write new unit tests to cover the untested code.
    *   **Refactor for Testability:** If some code is difficult to test, suggest refactoring strategies to improve its testability (e.g., dependency injection, pure functions).
3.  **Output Format:** Provide a Markdown document that outlines the steps to measure coverage and the strategy for improvement. Include example commands for generating the coverage report. For the improvement strategy, provide a prioritized list of files and specific recommendations for each.
