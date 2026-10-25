---
title: "Write an E2E Test for a Real-Time Collaboration Feature"
slug: write-an-e2e-test-for-a-real-time-collaboration-feature
stage: Test
category: "Testing & QA"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-an-e2e-test-for-a-real-time-collaboration-feature
---
# Write an E2E Test for a Real-Time Collaboration Feature

Write an E2E test script coordinating two user sessions to check bidirectional updates in a WebSocket-based collaboration feature.

## Prompt

Our application has a real-time collaboration feature (e.g., a collaborative text editor, a shared whiteboard) powered by WebSockets. I need an end-to-end test that simulates multiple users interacting with the feature simultaneously.

**Instructions:**
1.  **Testing Framework:** Use a framework that supports testing real-time applications, such as Cypress with a WebSocket testing plugin or Playwright with its multi-browser support.
2.  **Test Scenario:**
    1.  Open two separate browser instances or tabs.
    2.  Log in as two different users in each browser.
    3.  Navigate to the same collaborative session in both browsers.
    4.  In the first browser, perform an action (e.g., type some text, draw a shape).
    5.  In the second browser, assert that the action is reflected in real-time.
    6.  Repeat the process in the other direction (perform an action in the second browser and assert in the first).
3.  **Output Format:** Provide the complete E2E test script. The script must handle the complexity of coordinating actions and assertions between two concurrent browser sessions.
