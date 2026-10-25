---
title: "Data Encryption and Key Management Strategy for a Cloud Application"
slug: data-encryption-and-key-management-strategy-for-a-cloud-application
stage: Secure
category: "Security Review"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/data-encryption-and-key-management-strategy-for-a-cloud-application
---
# Data Encryption and Key Management Strategy for a Cloud Application

Architect a robust cloud-native encryption and key management strategy to secure PII at rest and in transit across all data services.

Variables: cloud_provider, database_service, storage_service, key_management_service

## Prompt

You are a security architect designing a data encryption and key management strategy for a new cloud-native application. The application will be deployed on {{cloud_provider}} and will handle Personally Identifiable Information (PII). Your strategy must ensure data is protected both at rest and in transit.

Please create a comprehensive document that outlines the following:

1.  **Data Classification:** Define different data sensitivity levels (e.g., Public, Internal, Confidential, Restricted) and map the application's data to these levels.
2.  **Encryption in Transit:** Specify the TLS/SSL configuration for all external and internal communication channels. Recommend strong cipher suites and certificate management practices.
3.  **Encryption at Rest:** Describe the encryption strategy for all data stores, including databases (e.g., {{database_service}}), object storage (e.g., {{storage_service}}), and backups. Specify the encryption algorithms to be used.
4.  **Key Management:** Propose a key management solution using a service like {{key_management_service}} (e.g., AWS KMS, Azure Key Vault, Google Cloud KMS). Detail the key hierarchy (e.g., Customer Master Keys, Data Encryption Keys), key rotation policies, and access control for key usage.

Your output should be a formal strategy document that can be used by the development and operations teams to implement the encryption and key management controls. The document should be well-organized, clear, and detailed.
