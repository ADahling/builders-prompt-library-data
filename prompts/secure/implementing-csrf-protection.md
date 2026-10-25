---
title: "Implementing CSRF Protection"
slug: implementing-csrf-protection
stage: Secure
category: "Security Checklist"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-csrf-protection
---
# Implementing CSRF Protection

Secure sensitive web endpoints by implementing robust CSRF token generation and validation within a specific framework.

Variables: web_framework

## Prompt

You are a mid-level engineer tasked with securing a web application against Cross-Site Request Forgery (CSRF) attacks. The application has several forms that perform sensitive actions, like changing a user's email address, but lacks any CSRF protection.

Context:
- The web framework is {{web_framework}}.
- A sensitive action is performed when a user submits a POST request to the `/update-email` endpoint.

Provide:
1. A clear explanation of what a CSRF attack is and why it's a threat.
2. A step-by-step guide on how to implement CSRF tokens (e.g., using a library like csurf or built-in framework features).
3. A code example showing how to add a CSRF token to a form and validate it on the server.

## Tips

Essential for securing any web application that manages user sessions and performs state-changing operations.
