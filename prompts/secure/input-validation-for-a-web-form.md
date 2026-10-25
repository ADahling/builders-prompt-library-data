---
title: "Input Validation for a Web Form"
slug: input-validation-for-a-web-form
stage: Secure
category: "Security Checklist"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/input-validation-for-a-web-form
---
# Input Validation for a Web Form

Implement robust server-side field validation to ensure data integrity and security across a specific backend framework.

Variables: form_fields, backend_framework

## Prompt

You are tasked with adding robust input validation to a user registration form. The form currently has minimal client-side validation, and no server-side validation, which could lead to data integrity issues and security vulnerabilities. You need to implement comprehensive validation on the server side.

Context:
- The form has the following fields: {{form_fields}}.
- The backend is built with {{backend_framework}}.

Provide:
1. A list of validation rules for each form field (e.g., username length, email format, password complexity).
2. A code example demonstrating how to perform server-side validation using a library like `express-validator` or `Joi`.
3. An explanation of why server-side validation is crucial even if you have client-side validation.

## Tips

A practical guide to one of the most fundamental aspects of web application security.
