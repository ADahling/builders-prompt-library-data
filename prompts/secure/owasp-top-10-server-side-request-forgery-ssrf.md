---
title: "OWASP Top 10: Server-Side Request Forgery (SSRF)"
slug: owasp-top-10-server-side-request-forgery-ssrf
stage: Secure
category: "Security Checklist"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/owasp-top-10-server-side-request-forgery-ssrf
---
# OWASP Top 10: Server-Side Request Forgery (SSRF)

Remediate Server-Side Request Forgery vulnerabilities by implementing URL validation and secure fetching patterns in your code.

Variables: user_supplied_url, programming_language

## Prompt

You are a developer who has been assigned a task to fix a Server-Side Request Forgery (SSRF) vulnerability in your application. The application has a feature that fetches an image from a URL provided by the user. An attacker can abuse this feature to make the server send requests to internal services.

Context:
- The vulnerable code takes a URL from the user as a parameter: `{{user_supplied_url}}`.
- The application is written in `{{programming_language}}`.

Provide:
1. An explanation of what an SSRF vulnerability is and the potential impact.
2. An example of a malicious URL that an attacker could provide to exploit this vulnerability (e.g., a URL pointing to an internal admin endpoint or a cloud provider's metadata service).
3. A code example showing how to fix the vulnerability by validating the user-supplied URL against a whitelist of allowed domains or by using a library designed to prevent SSRF.

## Tips

A practical prompt for understanding and fixing a serious and increasingly common vulnerability.
