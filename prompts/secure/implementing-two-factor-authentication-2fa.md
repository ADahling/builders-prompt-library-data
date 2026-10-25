---
title: "Implementing Two-Factor Authentication (2FA)"
slug: implementing-two-factor-authentication-2fa
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-two-factor-authentication-2fa
---
# Implementing Two-Factor Authentication (2FA)

Integrate TOTP-based two-factor authentication into a web application to enhance login security using library-driven code and QR generation.

Variables: web_framework, totp_library

## Prompt

You are tasked with adding Two-Factor Authentication (2FA) to a web application to enhance user security. The application currently relies only on username and password for authentication. Your goal is to implement Time-based One-Time Password (TOTP) as the second factor.

Context:
- The application is built with `{{web_framework}}`.
- You will use a library like `{{totp_library}}` to generate and verify TOTP codes.

Provide:
1. An explanation of how TOTP-based 2FA works.
2. A step-by-step guide on how to integrate the TOTP library into the login process, including generating a QR code for users to scan with an authenticator app.
3. A code example showing how to verify the TOTP code submitted by the user.

## Tips

A very practical prompt for adding a crucial security layer to any authentication system.
