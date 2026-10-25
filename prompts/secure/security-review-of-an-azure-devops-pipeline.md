---
title: "Security Review of an Azure DevOps Pipeline"
slug: security-review-of-an-azure-devops-pipeline
stage: Secure
category: "Security Review"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-review-of-an-azure-devops-pipeline
---
# Security Review of an Azure DevOps Pipeline

Conduct a comprehensive security audit of Azure DevOps CI/CD pipelines to identify vulnerabilities and implement hardening best practices.

Variables: project_name

## Prompt

You are a DevOps security engineer reviewing the security of an Azure DevOps pipeline for the {{project_name}} project. The pipeline builds and deploys a web application to Azure App Service. Your goal is to identify and mitigate security risks in the CI/CD process.

Create a detailed security review report in Markdown. The report should cover the following areas:

1.  **Source Code Protection:**
    *   Are there any branch protection rules in place for the main branch?
    *   Are there any secrets or sensitive data in the source code repository?

2.  **Build Security:**
    *   Is the build agent secure?
    *   Is the build process using a secure container image?
    *   Is there a process for scanning the source code and its dependencies for vulnerabilities (SAST and SCA)?

3.  **Release Security:**
    *   How are secrets and credentials managed in the release pipeline?
    *   Is there a manual approval step before deploying to production?
    *   Is the release pipeline using a secure connection to deploy the application?

4.  **Infrastructure Security:**
    *   Is the Azure App Service configured securely?
    *   Is the application using a managed identity to access other Azure resources?

For each area, provide your assessment and a list of prioritized recommendations for improvement. Your report should be a practical guide for the DevOps team to improve the security of their pipeline.
