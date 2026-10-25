---
title: "Compliance Automation for SOC 2 in an AWS Environment"
slug: compliance-automation-for-soc-2-in-an-aws-environment
stage: Secure
category: "Security Review"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/compliance-automation-for-soc-2-in-an-aws-environment
---
# Compliance Automation for SOC 2 in an AWS Environment

Automate SOC 2 compliance in AWS by mapping controls to services, scripting evidence collection, and configuring continuous monitoring.

## Prompt

You are a compliance specialist responsible for automating SOC 2 evidence collection in an AWS environment. Your task is to create a plan and provide scripts to continuously monitor and gather evidence for the SOC 2 Trust Services Criteria (Security, Availability, Processing Integrity, Confidentiality, and Privacy).

Your plan should address the following:

1.  **Control Mapping:** Map the SOC 2 criteria to specific AWS services and configurations (e.g., mapping the Security criteria to IAM policies, security groups, and CloudTrail logging).
2.  **Automated Evidence Collection:** Write scripts using the AWS CLI or SDKs (e.g., in Python with Boto3) to automatically collect evidence. For example, a script to check that all S3 buckets are encrypted, or that MFA is enabled for all IAM users.
3.  **Continuous Monitoring and Alerting:** Use AWS services like AWS Config and Security Hub to continuously monitor for compliance violations. Set up alerts to notify the team when a control fails.
4.  **Reporting Dashboard:** Propose a solution for a compliance reporting dashboard that provides a real-time view of the compliance posture and allows for easy evidence export for auditors.

Your output should be a detailed implementation guide, including the control mapping, the evidence collection scripts, and the configuration for the monitoring and alerting services. The guide should be practical and actionable for a DevOps team.
