---
title: "Advanced XSS Protection with CSP"
slug: advanced-xss-protection-with-csp
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-xss-protection-with-csp
---
# Advanced XSS Protection with CSP

Engineer a restrictive, source-specific Content Security Policy using nonces and advanced directives to eliminate XSS vulnerabilities.

Variables: frontend_framework, list_of_sources

## Prompt

You are a senior security engineer tasked with implementing a strict Content Security Policy (CSP) to mitigate the risk of XSS attacks. The application has a complex frontend with various scripts and styles loaded from different sources. Your goal is to create a CSP that is as restrictive as possible without breaking the application's functionality.

Context:
- The application is a single-page application (SPA) built with `{{frontend_framework}}`.
- The application loads resources from `{{list_of_sources}}`.

Provide:
1. A detailed explanation of advanced CSP directives like `script-src-elem`, `style-src-attr`, and `require-trusted-types-for`.
2. A strict CSP that you would recommend for this application, including the use of nonces or hashes for inline scripts.
3. A strategy for deploying the CSP in report-only mode first to identify any issues before enforcing it.

## Tips

An advanced prompt for experienced developers and security professionals looking to implement a robust defense against XSS.
