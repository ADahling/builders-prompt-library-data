---
title: "Secure File Uploads"
slug: secure-file-uploads
stage: Secure
category: "Security Checklist"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/secure-file-uploads
---
# Secure File Uploads

Secure profile picture uploads by implementing validation rules and file renaming to prevent remote code execution and directory traversal.

Variables: programming_language, upload_directory

## Prompt

You are developing a feature that allows users to upload profile pictures. However, the current implementation is insecure and could allow attackers to upload malicious files. Your task is to secure the file upload functionality to prevent common vulnerabilities like arbitrary file upload and remote code execution.

Context:
- The file upload endpoint is `/upload-avatar`.
- The application is written in `{{programming_language}}`.
- Uploaded files are stored in `{{upload_directory}}`.

Provide:
1. A list of potential security risks associated with file uploads.
2. A set of validation rules to apply to uploaded files (e.g., file type, size, and name).
3. A code snippet demonstrating how to securely process and store an uploaded file, including renaming the file to prevent directory traversal attacks.

## Tips

An essential prompt for any application that allows users to upload files.
