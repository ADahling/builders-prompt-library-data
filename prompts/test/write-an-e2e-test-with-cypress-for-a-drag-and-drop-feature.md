---
title: "Write an E2E Test with Cypress for a Drag-and-Drop Feature"
slug: write-an-e2e-test-with-cypress-for-a-drag-and-drop-feature
stage: Test
category: "Testing & QA"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-an-e2e-test-with-cypress-for-a-drag-and-drop-feature
---
# Write an E2E Test with Cypress for a Drag-and-Drop Feature

Generate comprehensive Cypress E2E scripts and assertions to validate drag-and-drop functionality and UI persistence in web applications.

Variables: user_action, drag_and_drop_library, application_type

## Prompt

You are a frontend QA engineer. Your task is to write an E2E test with Cypress for a drag-and-drop feature that allows users to {{user_action}}. The feature is implemented using {{drag_and_drop_library}}.

Context:
- The application is a {{application_type}} where users can organize items by dragging and dropping them.
- You need to test that the drag-and-drop functionality works as expected and that the changes are saved correctly.

Provide:
1. A Cypress script that simulates the drag-and-drop operation.
2. Assertions to verify that the item is moved to the correct position and that the UI is updated accordingly.
3. A test case to handle the scenario where the drop is invalid.

## Tips

A prompt for QA engineers who want to practice testing complex UI interactions like drag-and-drop with Cypress.
