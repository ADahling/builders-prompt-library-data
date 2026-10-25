---
title: "Perform Security Code Review for a Web Application"
slug: perform-security-code-review-for-a-web-application
stage: Test
category: "Testing & QA"
grade: B
score: 73
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/perform-security-code-review-for-a-web-application
---
# Perform Security Code Review for a Web Application

Identify and remediate security vulnerabilities in web applications using manual analysis and SAST tools to improve overall code security.

Variables: programming_language, vulnerability_1, vulnerability_2, vulnerability_3

## Prompt

You are a security analyst. Your task is to perform a security code review for a web application to identify any security vulnerabilities in the code. The application is written in {{programming_language}}.

Context:
- You will manually review the code and look for common security vulnerabilities, such as {{vulnerability_1}}, {{vulnerability_2}}, and {{vulnerability_3}}.
- You will also use a static analysis security testing (SAST) tool to scan the code for potential vulnerabilities.

Provide:
1. A report with all the security vulnerabilities found in the code, with their severity and location.
2. Recommendations for fixing the vulnerabilities, with code examples where applicable.
3. A summary of the overall security posture of the application.

## Tips

A prompt for security analysts and developers to practice security code review, which is an important step in building secure applications.
