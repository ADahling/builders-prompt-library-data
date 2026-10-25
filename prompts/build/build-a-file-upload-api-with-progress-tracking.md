---
title: "Build a File Upload API with Progress Tracking"
slug: build-a-file-upload-api-with-progress-tracking
stage: Build
category: "API Design"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-file-upload-api-with-progress-tracking
---
# Build a File Upload API with Progress Tracking

Implement a full-stack file upload system featuring real-time progress tracking, secure backend processing, and frontend UI updates.

Variables: app_type, backend_tech, frontend_tech, cloud_storage_service

## Prompt

You are a full-stack developer. I need to build a feature in my {{app_type}} application that allows users to upload large files. The API should be built with {{backend_tech}} and the frontend with {{frontend_tech}}. A key requirement is to show a real-time progress bar to the user during the upload.

**Task:**
Provide a guide on how to build a file upload API that supports large files and provides progress information.

**Instructions:**

1.  **Backend:**
    *   Choose a suitable library for handling multipart/form-data (e.g., 'multer' for Node.js).
    *   Show how to configure the backend to accept file uploads and save them to a temporary directory or a cloud storage service like {{cloud_storage_service}}.
    *   Explain how to handle potential errors during the upload (e.g., file too large, wrong file type).
2.  **Frontend:**
    *   Show how to use JavaScript (e.g., with 'axios' or the native 'fetch' API) to send the file to the backend API.
    *   Demonstrate how to listen to upload progress events (e.g., using the 'onUploadProgress' option in axios) and update a UI progress bar accordingly.
3.  **Security:** Briefly mention security considerations for file uploads, such as validating file types and scanning for malware.

**Output Format:**
Provide code examples for both the backend API endpoint and the frontend JavaScript code. The code should be well-commented to explain each part of the process.
