---
title: "Secure Coding Guidelines for an Application"
slug: secure-coding-guidelines-for-a-language-application
stage: Secure
category: "Security Review"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/secure-coding-guidelines-for-a-language-application
---
# Secure Coding Guidelines for an Application

Write a Markdown secure coding guide for your team's language, organized by OWASP vulnerability type with insecure and secure code examples.

Variables: language

## Prompt

You are a senior developer creating a set of secure coding guidelines for your team. The team develops applications in {{language}}. The goal is to provide developers with a clear and concise set of rules to follow to avoid common security vulnerabilities.

Create a secure coding guidelines document in Markdown. The document should be organized by vulnerability type and should include code examples of both insecure and secure code.

The guidelines should cover the following OWASP Top 10 vulnerabilities:

1.  **Injection:** How to prevent SQL injection, NoSQL injection, and command injection.
2.  **Broken Authentication:** How to securely implement authentication and session management.
3.  **Sensitive Data Exposure:** How to protect sensitive data in transit and at rest.
4.  **XML External Entities (XXE):** How to prevent XXE attacks.
5.  **Broken Access Control:** How to properly enforce access control.
6.  **Security Misconfiguration:** How to securely configure your application and servers.
7.  **Cross-Site Scripting (XSS):** How to prevent reflected, stored, and DOM-based XSS.
8.  **Insecure Deserialization:** How to prevent insecure deserialization vulnerabilities.
9.  **Using Components with Known Vulnerabilities:** How to manage and update third-party dependencies.
10. **Insufficient Logging and Monitoring:** How to properly log and monitor your application for security events.

For each vulnerability, provide a brief explanation of the vulnerability, a code example of how it can be exploited, and a code example of how to prevent it. Your guidelines should be a practical and valuable resource for your team.
