---
title: "GDPR Compliance: Data Anonymization"
slug: gdpr-compliance-data-anonymization
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/gdpr-compliance-data-anonymization
---
# GDPR Compliance: Data Anonymization

Develop a GDPR-compliant data anonymization strategy for sensitive database fields to ensure legal privacy while maintaining analytical utility.

Variables: database_type, sensitive_fields

## Prompt

You are a data engineer working for a company that needs to comply with the General Data Protection Regulation (GDPR). You have a large dataset containing user information that you need to anonymize before it can be used for analytics. Your task is to develop a strategy for anonymizing the data while preserving its utility.

Context:
- The dataset is stored in a `{{database_type}}` database.
- The sensitive data fields include `{{sensitive_fields}}`.

Provide:
1. An explanation of the difference between anonymization and pseudonymization under GDPR.
2. A list of at least three data anonymization techniques (e.g., generalization, suppression, k-anonymity).
3. A high-level plan for how you would apply these techniques to the given dataset, including any tools or libraries you would use.

## Tips

A challenging prompt that addresses the complex topic of data privacy and compliance.
