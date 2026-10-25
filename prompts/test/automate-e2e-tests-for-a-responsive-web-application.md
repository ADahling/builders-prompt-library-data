---
title: "Automate E2E Tests for a Responsive Web Application"
slug: automate-e2e-tests-for-a-responsive-web-application
stage: Test
category: "Testing & QA"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/automate-e2e-tests-for-a-responsive-web-application
---
# Automate E2E Tests for a Responsive Web Application

Get a test runner configuration and an adapted E2E test example for a responsive web app, covering multiple viewports and conditional UI interactions.

Variables: viewports

## Prompt

Our web application is designed to be responsive and work on various screen sizes. I need to automate our end-to-end tests to run against different viewports (e.g., mobile, tablet, desktop).

**Instructions:**
1.  **Testing Framework:** Use a framework that supports responsive testing, such as Cypress or Playwright.
2.  **Viewports:** The target viewports are: `{{viewports}}` (e.g., `375x667` for mobile, `768x1024` for tablet, `1920x1080` for desktop).
3.  **Test Adaptation:**
    *   Review our existing E2E tests and identify any that need to be adapted for different viewports.
    *   For example, on a mobile viewport, a navigation menu might be hidden behind a hamburger icon, so the test needs to click the icon first to open the menu.
4.  **Test Execution:** Configure the test runner to execute the test suite for each specified viewport.
5.  **Output Format:** Provide a configuration file for the test runner that sets up the different viewports. Also, provide an example of a test script that has been adapted to work across multiple viewports, using conditional logic if necessary to handle UI differences.
