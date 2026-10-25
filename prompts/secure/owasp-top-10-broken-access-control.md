---
title: "OWASP Top 10: Broken Access Control"
slug: owasp-top-10-broken-access-control
stage: Secure
category: "Security Checklist"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/owasp-top-10-broken-access-control
---
# OWASP Top 10: Broken Access Control

Implement role-based access control in a specific backend framework to secure administrative routes and enforce the principle of least privilege.

Variables: user_role, backend_framework

## Prompt

You are a security-conscious developer tasked with fixing a broken access control vulnerability in a web application. The application allows any authenticated user to access administrative functions by simply navigating to the admin URL. Your task is to implement proper access control to restrict access to authorized users only.

Context:
- The admin section is located at `/admin`.
- The user's role is available in the session as `{{user_role}}`.
- The backend is built with `{{backend_framework}}`.

Provide:
1. An explanation of the principle of least privilege and why it is important for access control.
2. A code example demonstrating how to add a middleware or a check to protect the `/admin` route, ensuring only users with the 'admin' role can access it.
3. A suggestion on how to manage roles and permissions in a more scalable way.

## Tips

A practical prompt for understanding and fixing one of the most common and critical web vulnerabilities.
