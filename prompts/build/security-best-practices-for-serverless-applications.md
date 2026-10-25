---
title: "Security Best Practices for Serverless Applications"
slug: security-best-practices-for-serverless-applications
stage: Build
category: "System Architecture"
grade: B
score: 75
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-best-practices-for-serverless-applications
---
# Security Best Practices for Serverless Applications

Produce a comprehensive security checklist for serverless applications that emphasizes least-privilege IAM policies and dependency scanning.

Variables: cloud_provider

## Prompt

You are a security engineer responsible for auditing a new serverless application built on {{cloud_provider}}. You need to provide the development team with a set of security best practices.

**Your Task:**
Create a comprehensive security checklist for serverless applications.

**Instructions & Constraints:**
1.  **The Principle of Least Privilege:**
    *   This is the most important security principle for serverless. Explain that each Lambda/Function should have an execution role with the absolute minimum permissions it needs to do its job.
    *   Provide an example of a good, narrowly-scoped IAM policy versus a bad, overly-permissive one.

2.  **Securing the Function Code:**
    *   **Dependency Scanning:** Emphasize the need to scan application dependencies for known vulnerabilities (e.g., using `npm audit
