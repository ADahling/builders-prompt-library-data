---
title: "Write Advanced Unit Tests for a Redux Reducer"
slug: write-advanced-unit-tests-for-a-redux-reducer
stage: Test
category: "Testing & QA"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-advanced-unit-tests-for-a-redux-reducer
---
# Write Advanced Unit Tests for a Redux Reducer

Get a Jest test file for a complex Redux reducer covering initial state, action payloads, unknown actions, and state immutability.

Variables: feature_name, reducer_code, action_types

## Prompt

I need a comprehensive suite of unit tests for a complex Redux reducer that manages the `{{feature_name}}` feature state in our application. The reducer handles multiple actions and involves nested state updates.

**Instructions:**
1.  **Reducer Code:**
    ```javascript
    {{reducer_code}}
    ```
2.  **Actions:** The reducer handles the following actions: `{{action_types}}`.
3.  **Test Scenarios:**
    *   **Initial State:** Test that the reducer returns the correct initial state when called with an undefined state.
    *   **Known Actions:** For each action type, write a test to verify that the state is updated correctly. Test with various payloads.
    *   **Unknown Actions:** Test that the reducer returns the current state when it receives an unknown action type.
    *   **Immutability:** Ensure that the reducer does not mutate the original state. Use a library like `deep-freeze` or write manual checks to enforce this.
4.  **Output Format:** Provide the complete Jest test file. The tests should be well-organized, with a `describe` block for the reducer and nested `describe` blocks for each action type.
