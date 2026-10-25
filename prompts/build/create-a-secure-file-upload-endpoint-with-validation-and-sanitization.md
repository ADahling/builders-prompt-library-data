---
title: "Create a Secure File Upload Endpoint with Validation and Sanitization"
slug: create-a-secure-file-upload-endpoint-with-validation-and-sanitization
stage: Build
category: "Backend & Data Integrity"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-secure-file-upload-endpoint-with-validation-and-sanitization
---
# Create a Secure File Upload Endpoint with Validation and Sanitization

Get a file upload endpoint guide and code with type and size validation, filename sanitization, storage guidance, and virus scanning suggestions.

Variables: application_type, programming_language

## Prompt

I need to create a secure file upload endpoint for my {{application_type}} application. Users should be able to upload files of certain types and sizes. I am concerned about security vulnerabilities like arbitrary file uploads and directory traversal attacks. The backend is written in {{programming_language}}.

Your task is to design and provide a guide for creating a secure file upload endpoint. The guide should cover:

1.  **File Type and Size Validation:** Show how to validate the file type (e.g., by checking the MIME type) and the file size to ensure that users can only upload allowed files.
2.  **Filename Sanitization:** Explain how to sanitize the filename to prevent directory traversal attacks and other issues. This should include removing special characters and generating a unique filename for each uploaded file.
3.  **Secure Storage:** Recommend a secure way to store the uploaded files. This could be on the local filesystem (with proper permissions) or in a cloud storage service like Amazon S3.
4.  **Code Example:** Provide a complete code example of a file upload endpoint that implements all the security measures mentioned above. The example should use a popular library for handling file uploads (e.g., Multer for Node.js, or the built-in functionality of your framework).
5.  **Virus Scanning:** Suggest how to integrate a virus scanner to scan uploaded files for malware.

## Tips

This prompt is essential for any developer building an application that accepts file uploads from users.
