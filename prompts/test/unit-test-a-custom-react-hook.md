---
title: "Unit Test a Custom React Hook"
slug: unit-test-a-custom-react-hook
stage: Test
category: "Testing & QA"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/unit-test-a-custom-react-hook
---
# Unit Test a Custom React Hook

Write a complete Jest test file for a custom React hook, covering initial state, updates, lifecycle behavior, and asynchronous logic.

Variables: hook_name, hook_logic, hook_code

## Prompt

I have created a custom React hook, `{{hook_name}}`, that encapsulates `{{hook_logic}}`. I need to write unit tests to ensure the hook behaves as expected.

**Instructions:**
1.  **Hook Code:**
    ```javascript
    {{hook_code}}
    ```
2.  **Testing Library:** Use `@testing-library/react-hooks`.
3.  **Test Scenarios:**
    *   **Initial State:** Test the hook's initial return values.
    *   **State Updates:** Test that the hook's state updates correctly in response to events or function calls.
    *   **Lifecycle:** Test the hook's behavior during mount, unmount, and re-render.
    *   **Asynchronous Logic:** If the hook contains asynchronous logic, use `waitForNextUpdate` to test the resolved state.
4.  **Output Format:** Provide the complete Jest test file. Use the `renderHook` and `act` utilities from `@testing-library/react-hooks` to test the hook in isolation.
