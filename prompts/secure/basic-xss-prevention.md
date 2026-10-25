---
title: "Basic XSS Prevention"
slug: basic-xss-prevention
stage: Secure
category: "Security Checklist"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/basic-xss-prevention
---
# Basic XSS Prevention

Secure web applications against cross-site scripting by implementing proper input sanitization and output encoding in a specific backend.

Variables: comment_field, backend_language

## Prompt

You are a junior developer learning about web security. Your task is to prevent basic Cross-Site Scripting (XSS) attacks in a web application. The application currently renders user-supplied input directly to the page, which is a major vulnerability. You need to properly sanitize the input before it is displayed.

Context:
- The user input is coming from a comment form field: {{comment_field}}.
- The backend is written in {{backend_language}}.

Provide:
1. An explanation of why rendering raw user input is dangerous.
2. A code snippet demonstrating how to sanitize the user input before rendering it in the browser.
3. A brief description of a library or function you can use for sanitization in {{backend_language}}.

## Tips

This prompt is ideal for developers new to security, focusing on the most common web vulnerability.
