---
title: "Create a Unit Test Plan for a New React Component"
slug: create-a-unit-test-plan-for-a-new-react-component
stage: Test
category: "Testing & QA"
grade: A+
score: 98
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-unit-test-plan-for-a-new-react-component
---
# Create a Unit Test Plan for a New React Component

Generate a comprehensive unit test plan with prioritized scenarios and mocking strategies to guide the test-driven development of a React component.

Variables: component_name, application_name, component_functionality

## Prompt

I am developing a new React component called `{{component_name}}` for our `{{application_name}}` application. The component is responsible for `{{component_functionality}}`. Before I start writing the implementation, I need a detailed unit test plan to guide my development (Test-Driven Development approach).

**Instructions:**
1.  **Identify Test Scenarios:** Analyze the component's requirements and identify all possible user interactions, states, and props. Create a comprehensive list of test scenarios.
2.  **Define Test Cases:** For each scenario, define specific test cases with clear inputs (props, state) and expected outputs (rendered UI, state changes, function calls).
3.  **Prioritize Tests:** Categorize the test cases into "critical path" (must-have for initial implementation) and "secondary" (can be added later).
4.  **Mocking Strategy:** Describe the strategy for mocking any external dependencies, such as API calls, hooks, or context providers.
5.  **Output Format:** Present the test plan in a structured Markdown document. Use headings for scenarios and bullet points for individual test cases. For each test case, specify the props, the action to be performed, and the expected result.
