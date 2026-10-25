---
title: "Implement Snapshot Testing for a React Component"
slug: implement-snapshot-testing-for-a-react-component
stage: Test
category: "Testing & QA"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-snapshot-testing-for-a-react-component
---
# Implement Snapshot Testing for a React Component

Get a Jest snapshot test file for a design system React component, covering two prop states and explaining how to update snapshots.

Variables: component_name, component_code

## Prompt

I want to implement snapshot testing for my React component, `{{component_name}}`, to prevent unintentional UI changes. The component is part of a design system and its visual consistency is critical.

**Instructions:**
1.  **Component Code:**
    ```javascript
    {{component_code}}
    ```
2.  **Testing Framework:** Use Jest and `react-test-renderer`.
3.  **Test Implementation:**
    *   Create a new test file: `{{component_name}}.test.js`.
    *   Write a test case that renders the component with a set of default props.
    *   Generate the initial snapshot.
    *   Write a second test case that renders the component with a different set of props to create a separate snapshot for that state.
4.  **Output Format:** Provide the complete test file as a single code block. Include a brief explanation of how snapshot testing works and how to update snapshots when intentional changes are made.
