---
title: "Security Code Review: Finding Vulnerabilities"
slug: security-code-review-finding-vulnerabilities
stage: Secure
category: "Security Checklist"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-code-review-finding-vulnerabilities
---
# Security Code Review: Finding Vulnerabilities

Audit pull requests for security flaws using a specialized vulnerability checklist and structured reporting template for safer deployments.

Variables: programming_language, list_of_files

## Prompt

You are a developer participating in a security code review. Your task is to review a pull request for potential security vulnerabilities. The pull request introduces a new feature that allows users to comment on articles.

Context:
- The code is written in `{{programming_language}}`.
- The pull request contains changes to the `{{list_of_files}}` files.

Provide:
1. A checklist of common security vulnerabilities to look for in a web application (e.g., XSS, SQL injection, CSRF, insecure direct object references).
2. For each item on the checklist, describe what you would look for in the code to identify that vulnerability.
3. A template for how to report a security finding in a code review in a constructive and helpful way.

## Tips

A practical guide for developers on how to perform effective security code reviews.
