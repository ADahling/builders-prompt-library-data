---
title: "Design an API for a File Upload and Processing Service"
slug: design-an-api-for-a-file-upload-and-processing-service
stage: Build
category: "API Design"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-file-upload-and-processing-service
---
# Design an API for a File Upload and Processing Service

Architect a RESTful file processing API featuring multipart upload endpoints, status tracking, and asynchronous backend job workflows.

## Prompt

I am building a service that allows users to upload files, which are then processed asynchronously. I need to design an API for this service.

Your task is to design the API endpoints for uploading files and checking the status of the processing job.

**Instructions:**
1.  **File Upload:** Design an API endpoint for uploading files. This should be a multi-part form data request. The response should include a job ID that can be used to track the status of the processing.
2.  **Job Status:** Design an API endpoint for checking the status of a processing job. The response should indicate whether the job is pending, in progress, completed, or failed. If the job is completed, the response should include a URL to the processed file.
3.  **Asynchronous Workflow:** Describe the asynchronous workflow from the moment a file is uploaded until it is processed and the user is notified. You can use a diagram to illustrate the workflow.

**Output Format:**
Provide the output as a Markdown document. For each API endpoint, specify the HTTP method, URI, request format, and response format. Also, include a diagram illustrating the asynchronous workflow.
