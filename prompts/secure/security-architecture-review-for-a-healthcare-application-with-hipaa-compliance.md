---
title: "Security Architecture Review for a Healthcare Application with HIPAA Compliance"
slug: security-architecture-review-for-a-healthcare-application-with-hipaa-compliance
stage: Secure
category: "Security Review"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-architecture-review-for-a-healthcare-application-with-hipaa-compliance
---
# Security Architecture Review for a Healthcare Application with HIPAA Compliance

Evaluate telehealth application architectures against HIPAA standards to identify security gaps and generate actionable compliance reports.

Variables: app_name

## Prompt

You are a senior security architect reviewing the security architecture of a new telehealth application, {{app_name}}, which must be compliant with HIPAA. The application allows patients to have video consultations with doctors and stores electronic health records (EHR).

Your task is to conduct a thorough review of the application's architecture to ensure it meets HIPAA's security and privacy requirements. Your review should be documented in a formal report.

The report must cover the following areas:

1.  **Access Control:**
    *   Review the role-based access control (RBAC) model. Ensure that only authorized individuals can access patient data and that access is based on the principle of minimum necessary use.

2.  **Encryption:**
    *   Verify that all protected health information (PHI) is encrypted both in transit (using TLS 1.2 or higher) and at rest (using AES-256 or equivalent).
    *   Review the key management strategy.

3.  **Audit Controls:**
    *   Ensure that all access to PHI is logged in a secure, immutable audit trail. The audit logs should record who accessed the data, when it was accessed, and what was done with it.

4.  **Data Integrity:**
    *   Review the mechanisms in place to protect the integrity of PHI from unauthorized alteration or destruction.

5.  **Transmission Security:**
    *   Assess the security of the video consultation feature. Ensure that the video stream is encrypted and that there are measures to prevent eavesdropping.

6.  **Contingency Plan:**
    *   Review the disaster recovery and business continuity plans to ensure that PHI can be recovered in the event of a disaster.

For each area, you must assess the current design, identify any gaps in compliance, and provide specific, actionable recommendations for remediation. Your report should serve as a guide for the development team to achieve HIPAA compliance.
