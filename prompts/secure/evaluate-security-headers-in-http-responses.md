---
title: "Evaluate Security Headers in HTTP Responses"
slug: evaluate-security-headers-in-http-responses
stage: Secure
category: "Security Review"
grade: C
score: 64
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/evaluate-security-headers-in-http-responses
---
# Evaluate Security Headers in HTTP Responses

Review an application's HTTP security headers and get suggestions for missing or misconfigured CSP, content type, and frame protections.

Variables: url

## Prompt

Check the HTTP response headers for the application hosted at {{url}}. Ensure that security headers such as Content-Security-Policy, X-Content-Type-Options, and X-Frame-Options are correctly implemented. Provide suggestions for any missing or misconfigured headers.

## Tips

Security headers are important for protecting against various attacks.
