---
title: "Infrastructure as Code (IaC) Security Review for AWS"
slug: infrastructure-as-code-iac-security-review-for-aws
stage: Secure
category: "Security Review"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/infrastructure-as-code-iac-security-review-for-aws
---
# Infrastructure as Code (IaC) Security Review for AWS

Audit IaC templates to identify AWS misconfigurations in IAM, networking, and storage while providing actionable remediation code.

Variables: iac_language

## Prompt

You are a cloud security specialist reviewing the Infrastructure as Code (IaC) templates for a new deployment on AWS. The IaC is written in {{iac_language}} (e.g., Terraform, CloudFormation). Your objective is to identify security misconfigurations and ensure the infrastructure is deployed according to security best practices.

Your review should focus on the following AWS services and security aspects:

*   **IAM (Identity and Access Management):** Check for overly permissive IAM roles and policies. Ensure the principle of least privilege is followed.
*   **VPC (Virtual Private Cloud):** Verify the network configuration, including security groups, network ACLs, and subnet routing. Ensure that no unnecessary ports are exposed to the internet.
*   **S3 (Simple Storage Service):** Check for public S3 buckets and ensure that encryption at rest is enabled.
*   **EC2 (Elastic Compute Cloud):** Review EC2 instance configurations, including the use of hardened AMIs, security groups, and SSH key management.
*   **RDS (Relational Database Service):** Ensure that RDS instances are not publicly accessible and that data encryption is enabled.

For each issue you find, provide:

*   **Finding:** A clear description of the misconfiguration.
*   **Risk:** An explanation of the potential security impact.
*   **Recommendation:** Specific code changes to the IaC template to fix the issue.

Your output should be a formal security review report in Markdown, with a summary of findings and a list of prioritized recommendations.
