---
title: "Create an Integration Test for a File Upload and Processing Feature"
slug: create-an-integration-test-for-a-file-upload-and-processing-feature
stage: Test
category: "Testing & QA"
grade: C
score: 63
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-integration-test-for-a-file-upload-and-processing-feature
---
# Create an Integration Test for a File Upload and Processing Feature

Get an integration test script for file uploads that automates the browser, tracks the API request, and checks processed data in the database.

## Prompt

Our application has a feature that allows users to upload a file, which is then processed by a backend service. I need to create an integration test to verify this entire workflow.

**Instructions:**
1.  **Feature Workflow:**
    1.  The user uploads a file via a web form.
    2.  The frontend sends the file to a REST API endpoint.
    3.  The backend service receives the file, processes it, and stores the result in a database.
2.  **Testing Framework:** Use a framework that can automate both browser interactions and API requests (e.g., Cypress, Playwright).
3.  **Test Implementation:**
    *   **Browser Automation:** The test should automate the process of visiting the web page, selecting a file to upload, and submitting the form.
    *   **API Request:** The test should intercept or track the API request to ensure the file is sent correctly.
    *   **Database Assertion:** After the upload, the test should query the database directly to verify that the processed data was stored correctly.
4.  **Output Format:** Provide the complete test script. The script should be well-structured and include comments explaining the different steps of the test.
