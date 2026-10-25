---
title: "SOC 2 Compliance: Audit Trail Implementation"
slug: soc-2-compliance-audit-trail-implementation
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/soc-2-compliance-audit-trail-implementation
---
# SOC 2 Compliance: Audit Trail Implementation

Design and implement a secure, tamper-proof audit logging system to satisfy SOC 2 compliance requirements for tracking sensitive user actions.

Variables: app_type, auditable_actions

## Prompt

You are a lead engineer preparing for a SOC 2 audit. One of the requirements is to have a comprehensive audit trail of all significant actions taken within your application. Your task is to design and implement an audit logging system that meets SOC 2 requirements.

Context:
- The application is a `{{app_type}}` that manages sensitive customer data.
- The key actions to be audited are `{{auditable_actions}}`.

Provide:
1. A list of the key data points that should be included in each audit log entry (e.g., timestamp, user ID, action, outcome, IP address).
2. A high-level design for the audit logging system, including how the logs will be generated, stored, and protected from tampering.
3. A code example of how to generate an audit log entry for a specific action.

## Tips

A practical prompt for engineers working on applications that need to meet SOC 2 compliance standards.
