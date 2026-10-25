---
title: "Write an E2E Test with Playwright for a File Upload Feature"
slug: write-an-e2e-test-with-playwright-for-a-file-upload-feature
stage: Test
category: "Testing & QA"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-an-e2e-test-with-playwright-for-a-file-upload-feature
---
# Write an E2E Test with Playwright for a File Upload Feature

Generate Playwright E2E scripts to validate file upload functionality, including successful processing and error handling for invalid files.

Variables: file_type, max_size, application_type

## Prompt

You are a QA automation engineer. Your task is to write an E2E test with Playwright for a feature that allows users to upload a file. The feature should accept files of type {{file_type}} and with a maximum size of {{max_size}}.

Context:
- The application is a {{application_type}} where users can upload documents or images.
- You need to test that the file is uploaded successfully and that the application handles invalid files correctly.

Provide:
1. A Playwright script that automates the file upload process.
2. A test case for a valid file that verifies that the file is uploaded and processed correctly.
3. Test cases for invalid files (e.g., wrong file type, file too large) to ensure proper error handling.

## Tips

A prompt for QA engineers who want to practice testing file upload features, which can be tricky to automate.
