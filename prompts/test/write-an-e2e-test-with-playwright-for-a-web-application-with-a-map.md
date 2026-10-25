---
title: "Write an E2E Test with Playwright for a Web Application with a Map"
slug: write-an-e2e-test-with-playwright-for-a-web-application-with-a-map
stage: Test
category: "Testing & QA"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-an-e2e-test-with-playwright-for-a-web-application-with-a-map
---
# Write an E2E Test with Playwright for a Web Application with a Map

Generate Playwright E2E tests for interactive maps to validate panning, zooming, marker actions, and failure handling across map libraries.

Variables: map_interaction, map_library

## Prompt

You are a senior QA automation engineer. Your task is to write an E2E test with Playwright for a web application that has an interactive map. The map allows users to {{map_interaction}}.

Context:
- The map is implemented using a library like {{map_library}}.
- You need to test that the map interactions work as expected and that the application state is updated correctly.

Provide:
1. A Playwright script that simulates user interactions with the map, such as panning, zooming, and clicking on markers.
2. Assertions to verify that the map displays the correct information and that the application responds to the map events.
3. A test case to handle the scenario where the map fails to load.

## Tips

An advanced prompt for QA engineers who want to test web applications with complex and interactive features like maps.
