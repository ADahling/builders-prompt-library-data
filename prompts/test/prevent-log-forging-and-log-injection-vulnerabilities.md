---
title: "Prevent Log Forging and Log Injection Vulnerabilities"
slug: prevent-log-forging-and-log-injection-vulnerabilities
stage: Test
category: "Cleanup & Warnings"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/prevent-log-forging-and-log-injection-vulnerabilities
---
# Prevent Log Forging and Log Injection Vulnerabilities

Get an explanation of log injection with attack examples, a sanitization function, and structured logging examples for apps that log user input.

Variables: language

## Prompt

My application logs user-supplied input for debugging and auditing purposes. For example, when a user fails to log in, we log their username: `log.warn("Failed login for user: " + username);`

I have been warned that this could be vulnerable to "log forging" or "log injection," where a malicious user could inject fake log messages by including newline characters or other control characters in their input.

Your task is to explain this vulnerability and show how to prevent it.

1.  **The Vulnerability Explained:** Explain how log forging works. Show an example where a malicious `username` like `hacker
INFO: User admin logged in successfully` could be used to inject a fake log entry, which could be used to confuse a system administrator or cover up an attack.
2.  **Prevention Techniques:** What is the best way to prevent this? Compare the following techniques:
    *   **Input Sanitization:** Stripping out newline characters and other control characters from any user input before it is logged. Provide a function to do this.
    *   **Structured Logging:** Explain why using a structured logging library (like Winston or Pino in Node.js) that logs in a format like JSON is the best defense. Show an example where the user input is logged as a property of a JSON object, not concatenated into the main message string. This way, the input is treated as data, not as part of the log message structure.
3.  **Code Examples:** Provide "bad" (vulnerable) and "good" (secure) code examples in `{{language}}`.
4.  **Linting:** Are there any static analysis tools or linters that can detect potential log forging vulnerabilities?

Output should be a security-focused guide for developers.

## Tips

A subtle but important security vulnerability that is often overlooked.
