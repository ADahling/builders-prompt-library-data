---
title: "Write a Test to Prevent Sensitive Data Exposure"
slug: write-a-test-to-prevent-sensitive-data-exposure
stage: Test
category: "Testing & QA"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-test-to-prevent-sensitive-data-exposure
---
# Write a Test to Prevent Sensitive Data Exposure

Create automated security tests and assertions to verify that sensitive information remains redacted in application logs and API responses.

Variables: sensitive_data_type

## Prompt

You are a security-conscious developer. Your task is to write a test to prevent sensitive data exposure in a web application. The application handles sensitive user data, such as {{sensitive_data_type}}, and you need to ensure that it is not accidentally exposed in logs, error messages, or API responses.

Context:
- You will write a test that triggers an error or an event that could potentially expose sensitive data.
- You will then inspect the logs, error messages, and API responses to ensure that the sensitive data is not present.

Provide:
1. A test that simulates a scenario where sensitive data could be exposed.
2. Assertions to verify that the sensitive data is not present in any of the outputs.
3. A recommendation for a secure coding practice to prevent sensitive data exposure.

## Tips

A prompt for developers to learn how to write tests to protect their applications from sensitive data exposure vulnerabilities.
