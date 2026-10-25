---
title: "OWASP Top 10: Broken Authentication"
slug: owasp-top-10-broken-authentication
stage: Secure
category: "Security Checklist"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/owasp-top-10-broken-authentication
---
# OWASP Top 10: Broken Authentication

Secure a web application against brute-force and credential stuffing attacks by implementing authentication controls and defensive code.

Variables: programming_language

## Prompt

You are a developer working on a web application's login page. You have been tasked with improving its security to prevent common authentication attacks. The current login page is vulnerable to brute-force and credential stuffing attacks.

Context:
- The login page is at `/login`.
- The backend is written in `{{programming_language}}`.

Provide:
1. An explanation of brute-force and credential stuffing attacks.
2. A list of security controls to implement to protect the login page, such as account lockout policies, CAPTCHA, and checking for breached passwords.
3. A code example or a high-level description of how to implement one of these controls.

## Tips

A practical prompt for securing one of the most critical parts of any web application.
