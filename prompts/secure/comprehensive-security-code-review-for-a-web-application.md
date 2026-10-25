---
title: "Comprehensive Security Code Review for a Web Application"
slug: comprehensive-security-code-review-for-a-web-application
stage: Secure
category: "Security Review"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/comprehensive-security-code-review-for-a-web-application
---
# Comprehensive Security Code Review for a Web Application

Conduct a rigorous security audit of a web application's codebase to detect, risk-rate, and remediate critical architectural vulnerabilities.

Variables: tech_stack

## Prompt

You are a senior security engineer performing a comprehensive security code review of a new web application. The application is built with the following technology stack: {{tech_stack}}. The primary goal is to identify and mitigate potential security vulnerabilities before deployment.

Your review should cover, but not be limited to, the following areas:

1.  **Input Validation and Sanitization:** Analyze all user-controllable inputs to prevent injection attacks (SQLi, XSS, Command Injection).
2.  **Authentication and Authorization:** Verify the implementation of user login, session management, and access control mechanisms. Ensure that password storage is secure (e.g., using bcrypt) and that proper authorization checks are in place for all sensitive operations.
3.  **Error Handling and Logging:** Review error messages to ensure they do not leak sensitive information. Check that all security-relevant events are logged in a structured and secure format.
4.  **Cryptography:** Assess the use of cryptographic functions for data encryption, ensuring that strong, up-to-date algorithms and proper key management practices are followed.
5.  **Insecure Direct Object References (IDOR):** Look for any instances where internal implementation objects, such as files or database keys, are exposed to users, allowing them to manipulate references and gain unauthorized access.

For each vulnerability you identify, provide the following:

*   **Vulnerability:** A clear and concise description of the security flaw.
*   **Location:** The specific file path and line number(s) where the vulnerability exists.
*   **Risk Rating:** A rating of the vulnerability's severity (Critical, High, Medium, or Low).
*   **Remediation:** Detailed, actionable steps to fix the vulnerability, including code examples where applicable.

Finally, provide a summary of your findings and an overall assessment of the application's security posture. Your output should be a well-structured Markdown report.
