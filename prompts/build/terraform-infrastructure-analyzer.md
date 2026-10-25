---
title: "Terraform Infrastructure Analyzer"
slug: terraform-infrastructure-analyzer
stage: Build
category: "DevOps & IaC"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/terraform-infrastructure-analyzer
---
# Terraform Infrastructure Analyzer

Audit Terraform files for security, cost, reliability, and configuration issues, with severity ratings and code for recommended changes.

## Prompt

Analyze my Terraform configuration for improvements:

1. SECURITY:
   - Are there any hardcoded secrets or credentials?
   - Are security groups / firewall rules too permissive?
   - Is encryption enabled for data at rest and in transit?
   - Are IAM policies following least privilege?

2. COST OPTIMIZATION:
   - Are instance types right-sized for the workload?
   - Are there unused or underutilized resources?
   - Can reserved instances or spot instances save money?
   - Are there resources running 24/7 that should be scheduled?

3. RELIABILITY:
   - Is there redundancy across availability zones?
   - Are backups configured and tested?
   - Is there auto-scaling for variable workloads?
   - What's the disaster recovery strategy?

4. BEST PRACTICES:
   - Are all resources tagged consistently?
   - Is state stored remotely with locking?
   - Are modules used for reusable components?
   - Are variables and outputs properly documented?

For each finding: severity, current state, recommended change, and the Terraform code to implement it.

My Terraform files: [paste or describe your infrastructure]

## Tips

Adapted from Firefly.ai's Terraform analysis prompts. Source: firefly.ai/academy/master-prompt-engineering-top-10
