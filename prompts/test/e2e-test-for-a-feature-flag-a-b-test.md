---
title: "E2E Test for a Feature Flag (A/B Test)"
slug: e2e-test-for-a-feature-flag-a-b-test
stage: Test
category: "Testing & QA"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/e2e-test-for-a-feature-flag-a-b-test
---
# E2E Test for a Feature Flag (A/B Test)

Write a complete E2E test script for a feature rollout, with flag controls and separate checks for enabled functionality and disabled visibility.

Variables: feature_name, e2e_framework

## Prompt

We are rolling out a new feature, `{{feature_name}}`, behind a feature flag. I need an end-to-end test to verify that the feature is correctly displayed or hidden based on the feature flag's state.

**Instructions:**
1.  **Testing Framework:** Use `{{e2e_framework}}`.
2.  **Feature Flag Control:** The test needs a way to control the feature flag's state. This could be done by setting a cookie, a `localStorage` item, or by making an API call to a feature flag management service.
3.  **Test Scenarios:**
    *   **Feature Flag Enabled:**
        1.  Enable the feature flag.
        2.  Navigate to the relevant page.
        3.  Assert that the new feature's UI is visible and functional.
    *   **Feature Flag Disabled:**
        1.  Disable the feature flag.
        2.  Navigate to the same page.
        3.  Assert that the new feature's UI is not present.
4.  **Output Format:** Provide the complete E2E test script. The script should include the logic for controlling the feature flag and should clearly separate the tests for the enabled and disabled states.
