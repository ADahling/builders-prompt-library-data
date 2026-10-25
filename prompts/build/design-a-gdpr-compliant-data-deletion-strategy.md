---
title: "Design a GDPR-Compliant Data Deletion Strategy"
slug: design-a-gdpr-compliant-data-deletion-strategy
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-gdpr-compliant-data-deletion-strategy
---
# Design a GDPR-Compliant Data Deletion Strategy

Plan user data deletion for GDPR requests with data discovery, backup handling, an idempotent deletion script, and verification.

Variables: application_name, tech_stack, database_type, scripting_language

## Prompt

Our application, {{application_name}}, needs to comply with the GDPR "right to be forgotten." This means we must be able to completely and permanently delete all data associated with a user upon their request. Our backend is built with {{tech_stack}} and uses a {{database_type}} database with many interconnected tables.

Your task is to design a comprehensive data deletion strategy that is both GDPR-compliant and technically sound. The design should include:

1.  **Data Discovery:** A plan for identifying all personal data related to a user across all our systems, including databases, logs, and third-party services.
2.  **Deletion Workflow:** A step-by-step workflow for deleting the user's data. This should address challenges like foreign key constraints, orphaned records, and data in backups.
3.  **Anonymization vs. Deletion:** A discussion of when it is appropriate to anonymize data instead of deleting it, and how to do so in a way that is irreversible.
4.  **Deletion Script:** A well-documented and robust script in {{scripting_language}} that automates the deletion process. The script should be idempotent and include thorough logging.
5.  **Verification:** A process for verifying that all of the user's data has been successfully deleted and for generating a certificate of deletion for the user.

## Tips

This prompt is critical for developers building applications for users in the EU, as it addresses a key requirement of GDPR.
