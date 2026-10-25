---
title: "Cloud Security: Securing S3 Buckets"
slug: cloud-security-securing-s3-buckets
stage: Secure
category: "Security Checklist"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/cloud-security-securing-s3-buckets
---
# Cloud Security: Securing S3 Buckets

Remediate public S3 bucket exposures and implement automated preventative policies using AWS CLI commands and JSON access controls.

Variables: list_of_public_buckets

## Prompt

You are a cloud security engineer who has discovered that several S3 buckets in your company's AWS account are publicly accessible. This is a major security risk that could lead to a data breach. Your task is to secure these S3 buckets and implement a policy to prevent this from happening again.

Context:
- You are using the AWS CLI or the AWS Management Console.
- The list of public S3 buckets is `{{list_of_public_buckets}}`.

Provide:
1. Step-by-step instructions on how to make a public S3 bucket private.
2. An S3 bucket policy (in JSON format) that denies all public access to the bucket, while still allowing access from specific IAM roles or IP addresses.
3. A recommendation for a preventative control, such as using AWS Config to automatically detect and remediate publicly accessible S3 buckets.

## Tips

A very practical and important prompt for anyone using AWS.
