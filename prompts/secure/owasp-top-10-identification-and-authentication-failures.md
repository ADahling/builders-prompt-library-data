---
title: "OWASP Top 10: Identification and Authentication Failures"
slug: owasp-top-10-identification-and-authentication-failures
stage: Secure
category: "Security Checklist"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/owasp-top-10-identification-and-authentication-failures
---
# OWASP Top 10: Identification and Authentication Failures

Audit a web application's authentication system to identify vulnerabilities and implement secure session management and credential protection.

Variables: app_type

## Prompt

You are reviewing the authentication system of a web application and have found several weaknesses. The application allows weak passwords, does not have proper session management, and is vulnerable to credential stuffing attacks. Your task is to propose a set of improvements to strengthen the authentication system.

Context:
- The application is a `{{app_type}}`.
- The current session management uses non-expiring session cookies.

Provide:
1. A list of the identified weaknesses in the authentication system.
2. For each weakness, propose a specific improvement (e.g., enforce strong password policies, implement secure session management with timeouts and renewal, add rate limiting to the login page).
3. A justification for why these improvements are important for security.

## Tips

A comprehensive prompt that covers several aspects of authentication security.
