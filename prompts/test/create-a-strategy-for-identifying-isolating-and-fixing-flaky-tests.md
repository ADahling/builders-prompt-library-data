---
title: "Create a Strategy for Identifying, Isolating, and Fixing Flaky Tests"
slug: create-a-strategy-for-identifying-isolating-and-fixing-flaky-tests
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-strategy-for-identifying-isolating-and-fixing-flaky-tests
---
# Create a Strategy for Identifying, Isolating, and Fixing Flaky Tests

Plan how to identify, quarantine, and diagnose flaky tests in a CI/CD pipeline, using build history, retries, and a root-cause checklist.

Variables: testing_framework

## Prompt

My project's CI/CD pipeline is unreliable because of "flaky" tests. These are tests that sometimes pass and sometimes fail for no apparent reason. This erodes the team's trust in the test suite, and developers are starting to ignore test failures.

I need a formal strategy for dealing with our flaky test problem. We are using `{{testing_framework}}`.

Your task is to create this strategy.

1.  **Identifying Flaky Tests:** How can we systematically identify which tests are flaky? Suggest a process:
    *   Analyze CI/CD build history to find tests that have failed and then passed on a retry without any code changes.
    *   Use the test runner's built-in retry functionality (if it has one) to automatically flag tests that only pass after a retry.
2.  **Isolating Flaky Tests:** Once a test is identified as flaky, we should not delete it, but we also can't let it block our pipeline. Propose a strategy for isolating it:
    *   Move the flaky test to a separate test suite (e.g., `describe.skip` or a separate file).
    *   Create a "quarantine" job in the CI pipeline that runs only the flaky tests but does not fail the build if they fail. This allows us to monitor their flakiness without blocking developers.
3.  **Diagnosing the Root Cause:** What are the common causes of flakiness? Provide a checklist for the developer who is assigned to fix the flaky test:
    *   **Race Conditions:** Tests that depend on the timing of asynchronous operations.
    *   **State Leakage:** A test that is not properly cleaning up after itself and is affecting a subsequent test.
    *   **External Dependencies:** A test that depends on a flaky or slow external service (e.g., a third-party API).
    *   **Time-based Logic:** A test that depends on the current time.
4.  **Fixing the Flakiness:** For each of the common causes, suggest a fix. (e.g., properly `await`ing async calls, using `beforeEach`/`afterEach` for cleanup, mocking external services, using a fake timer).

Output should be a formal process document for improving test suite reliability.

## Tips

Flaky tests are a cancer in a CI/CD pipeline. A systematic approach is needed to eradicate them.
