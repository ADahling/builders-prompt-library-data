---
title: "Write End-to-End Test Scenarios"
slug: write-end-to-end-test-scenarios
stage: Test
category: "Testing & QA"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-end-to-end-test-scenarios
---
# Write End-to-End Test Scenarios

Get Playwright tests for critical app journeys covering happy paths, errors, edge cases, and auth boundaries, with assertions and cleanup.

## Prompt

Write comprehensive E2E test scenarios for [describe app]:

For each critical user journey:
1. Test name and description.
2. Preconditions (user state, data state).
3. Step-by-step actions (click, type, navigate).
4. Assertions after each step.
5. Teardown (cleanup created data).

Cover:
- Happy path (everything works)
- Error path (invalid input, network failure)
- Edge case (empty state, max length, special characters)
- Auth boundaries (accessing other users' data)

Format as Playwright test code ready to run.

## Tips

Paste into your test files. Covers what manual testing misses.
