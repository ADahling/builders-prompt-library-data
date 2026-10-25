---
title: "Write a Test to Prevent Broken Authentication"
slug: write-a-test-to-prevent-broken-authentication
stage: Test
category: "Testing & QA"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-test-to-prevent-broken-authentication
---
# Write a Test to Prevent Broken Authentication

Create security tests to identify authentication bypass vulnerabilities and implement robust defenses against specific login attack vectors.

Variables: attack_vector

## Prompt

You are a security engineer. Your task is to write a test to prevent broken authentication vulnerabilities in a web application. The application has a login feature that is vulnerable to {{attack_vector}}.

Context:
- You need to ensure that the authentication mechanism is secure and cannot be bypassed.
- You will write a test that tries to exploit the vulnerability and gain unauthorized access to the application.

Provide:
1. A test that tries to bypass the authentication mechanism using the identified attack vector.
2. An assertion to verify that the application denies access and does not create a valid session.
3. A recommendation for a secure coding practice to prevent broken authentication vulnerabilities.

## Tips

A prompt for security engineers and developers to learn how to write tests to protect their applications from broken authentication vulnerabilities.
