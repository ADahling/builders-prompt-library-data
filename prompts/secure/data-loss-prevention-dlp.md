---
title: "Data Loss Prevention (DLP)"
slug: data-loss-prevention-dlp
stage: Secure
category: "Security Checklist"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/data-loss-prevention-dlp
---
# Data Loss Prevention (DLP)

Develop and deploy a basic email DLP policy and communication plan to prevent sensitive data leaks within Microsoft 365 or Google Workspace.

Variables: email_provider, sensitive_data_type

## Prompt

You are an IT manager who is concerned about the risk of sensitive data leaving the company's network. You want to implement a Data Loss Prevention (DLP) solution to mitigate this risk. Your task is to create a plan for implementing a basic DLP policy.

Context:
- The company uses `{{email_provider}}` (e.g., Microsoft 365, Google Workspace).
- You are concerned about employees accidentally or maliciously sending sensitive data, such as `{{sensitive_data_type}}`, to external parties.

Provide:
1. An explanation of what Data Loss Prevention (DLP) is.
2. A step-by-step guide on how to create a simple DLP policy in your chosen email provider that detects and blocks emails containing the sensitive data type.
3. A plan for how to communicate this new policy to employees and handle any false positives.

## Tips

A practical prompt for IT administrators and security managers on how to protect sensitive data.
