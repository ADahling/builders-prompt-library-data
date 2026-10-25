---
title: "HTTP Parameter Pollution (HPP)"
slug: http-parameter-pollution-hpp
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/http-parameter-pollution-hpp
---
# HTTP Parameter Pollution (HPP)

Demonstrate and remediate HTTP Parameter Pollution vulnerabilities by crafting bypass payloads tailored to specific backend frameworks.

Variables: backend_framework

## Prompt

You are a security tester who has discovered an HTTP Parameter Pollution (HPP) vulnerability in a web application. The application is not handling multiple occurrences of the same parameter in an HTTP request correctly, which can lead to unexpected behavior. Your task is to demonstrate and explain this vulnerability.

Context:
- The application has a feature that performs an action based on a URL parameter, e.g., `?action=view`.
- The backend is written in `{{backend_framework}}`.

Provide:
1. An explanation of what HTTP Parameter Pollution is and how it can occur.
2. An example of a malicious request that uses HPP to bypass a security control or cause unexpected behavior (e.g., `?action=view&action=delete`).
3. A recommendation on how the backend should handle duplicate parameters to prevent HPP vulnerabilities.

## Tips

A prompt that covers a less common but still important web security vulnerability.
