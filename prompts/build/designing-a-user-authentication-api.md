---
title: "Designing a User Authentication API"
slug: designing-a-user-authentication-api
stage: Build
category: "API Design"
grade: C
score: 68
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-user-authentication-api
---
# Designing a User Authentication API

Plan an authentication API for login, registration, and password resets, with request fields, responses, and security considerations.

Variables: login, registration, email, password

## Prompt

Outline a user authentication API for managing {{login}}, {{registration}}, and {passwordReset}. Include details on:
- Endpoint structures including {POST /login}, {POST /register}, and {POST /reset-password}.
- Required fields for each endpoint, such as {{email}}, {{password}}, and {newPassword}.
- Response structures for successful and failed authentication attempts.
- Security considerations such as using HTTPS, token management, and rate limiting.

## Tips

This prompt will assist you in designing a robust authentication system for your application.
