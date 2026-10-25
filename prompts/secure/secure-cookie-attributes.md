---
title: "Secure Cookie Attributes"
slug: secure-cookie-attributes
stage: Secure
category: "Security Checklist"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/secure-cookie-attributes
---
# Secure Cookie Attributes

Configure a session cookie with optimal security attributes and code examples to prevent session hijacking and cross-site attacks.

Variables: cookie_name

## Prompt

You are a web developer who is setting a session cookie for a user after they log in. You want to make sure the cookie is as secure as possible. Your task is to set the appropriate attributes for the session cookie.

Context:
- The application is served over HTTPS.
- The cookie is named `{{cookie_name}}`.

Provide:
1. A list of recommended security attributes for a session cookie (e.g., `Secure`, `HttpOnly`, `SameSite`).
2. For each attribute, explain what it does and why it is important for security.
3. A code example showing how to set these attributes when creating the cookie in your chosen web framework.

## Tips

A practical and often overlooked aspect of web security.
