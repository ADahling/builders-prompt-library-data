---
title: "Serverless Application Security Audit"
slug: serverless-application-security-audit
stage: Test
category: "Quality Audits"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/serverless-application-security-audit
---
# Serverless Application Security Audit

Generate a comprehensive security audit report for serverless applications by evaluating tech stacks against the OWASP Serverless Top 10.

Variables: project_name, project_description, tech_stack

## Prompt

As a cybersecurity analyst, I need you to perform a security audit of our serverless application, `{{project_name}}`. This application is a {{project_description}} built with {{tech_stack}}. The goal of this audit is to identify and prioritize security vulnerabilities based on the OWASP Serverless Top 10 and other common serverless application attack vectors.

Your audit should include, but not be limited to, the following areas:

1.  **Injection:** Look for any potential injection vulnerabilities in our serverless functions.

2.  **Broken Authentication:** Review the authentication and session management mechanisms.

3.  **Sensitive Data Exposure:** Identify any instances where sensitive data is not properly protected.

4.  **XML External Entities (XXE):** If the application processes XML input, check for XXE vulnerabilities.

5.  **Broken Access Control:** Review the access control implementation.

6.  **Security Misconfiguration:** Audit the security configuration of our serverless functions and other cloud resources.

7.  **Insecure Deserialization:** If the application uses serialization, check for insecure deserialization vulnerabilities.

8.  **Using Components with Known Vulnerabilities:** Check for the use of any third-party libraries or components with known security vulnerabilities.

9.  **Insufficient Logging & Monitoring:** Review the logging and monitoring capabilities of our serverless application.

10. **Improper Exception Handling:** Review the exception handling mechanisms in our serverless functions.

**Output Format:**

Please provide a detailed security audit report in Markdown format with the following sections:

*   **Executive Summary:** A high-level overview of the application's security posture and a summary of the most critical vulnerabilities found.
*   **Vulnerability Details:** A list of all identified vulnerabilities, ordered by severity. For each vulnerability, provide:
    *   **Vulnerability ID:** A unique identifier.
    *   **Severity:** (Critical, High, Medium, Low, Informational)
    *   **Description:** A detailed explanation of the vulnerability and how it can be exploited.
    *   **Proof of Concept:** A clear example or steps to reproduce the vulnerability.
    *   **Remediation:** Specific and actionable steps to fix the vulnerability, including code examples where appropriate.
*   **Recommendations:** A list of recommendations for improving the overall security of the application.

Your report should be clear, concise, and provide enough detail for our development team to understand and address the identified security risks.
