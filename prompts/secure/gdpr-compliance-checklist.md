---
title: "GDPR Compliance Checklist"
slug: gdpr-compliance-checklist
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/gdpr-compliance-checklist
---
# GDPR Compliance Checklist

Generate a tailored GDPR compliance roadmap with technical implementation guidance and code examples for specific application data activities.

Variables: application_name, data_activity_1, data_activity_2, data_activity_3

## Prompt

You are a data protection officer. Generate a GDPR compliance checklist for {{application_name}} that processes data of EU residents.

Data processing activities:
- {{data_activity_1}}
- {{data_activity_2}}
- {{data_activity_3}}

Checklist:
1. **Lawful Basis**: Document the lawful basis for each processing activity
2. **Privacy Notice**: Clear, accessible privacy policy in plain language
3. **Consent Management**: Cookie consent banner, preference center, withdrawal mechanism
4. **Data Subject Rights**: Implement right to access, rectification, erasure, portability
5. **Data Processing Agreements**: DPAs with all sub-processors (hosting, analytics, email)
6. **Data Protection Impact Assessment**: DPIA for high-risk processing
7. **Breach Notification**: 72-hour notification procedure
8. **Data Minimization**: Only collect what's necessary
9. **Retention Policy**: Define and enforce data retention periods
10. **International Transfers**: Standard Contractual Clauses for non-EU transfers
11. **Technical Measures**: Encryption, pseudonymization, access controls
12. **Record of Processing**: Maintain Article 30 records

For each item, provide implementation guidance and code examples where applicable.

## Tips

GDPR fines can reach 4% of global revenue. This checklist covers the essential requirements.
