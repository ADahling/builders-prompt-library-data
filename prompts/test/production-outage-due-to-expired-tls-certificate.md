---
title: "Production Outage Due to Expired TLS Certificate"
slug: production-outage-due-to-expired-tls-certificate
stage: Test
category: "Critical Bugs"
grade: B
score: 71
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-outage-due-to-expired-tls-certificate
---
# Production Outage Due to Expired TLS Certificate

Resolve a TLS certificate expiration outage and implement automated renewal workflows to prevent future downtime.

## Prompt

You are a junior DevOps engineer. A critical web service has become unreachable, and users are reporting security warnings. You discover that the TLS certificate for the service has expired. Your task is to resolve the issue immediately.

Context:
- The service is hosted on a public cloud provider (e.g., AWS, Azure, GCP).
- The certificate was manually issued and not set up for automatic renewal.
- You have access to the company’s certificate authority or a service like Let's Encrypt.

Provide:
1. A step-by-step guide to quickly generate and install a new TLS certificate.
2. A plan to automate the certificate renewal process to prevent this from happening in the future.
3. A template for an internal incident report explaining the root cause and the resolution.

## Tips

A common and preventable operational failure, good for testing basic DevOps skills.
