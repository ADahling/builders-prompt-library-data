---
title: "Troubleshoot DNS Issues"
slug: troubleshoot-dns-issues
stage: Ship
category: "Deployment & Launch"
grade: C
score: 67
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/troubleshoot-dns-issues
---
# Troubleshoot DNS Issues

Diagnose and resolve website connectivity problems by systematically verifying DNS record accuracy, resolution functionality, and provider status.

Variables: website_url

## Prompt

You are a help desk technician. A user is reporting that they cannot access your company's website, `{{website_url}}`. Your task is to troubleshoot the potential DNS issue.

Instructions:
1. Use tools like `dig` or `nslookup` to check the DNS records for the domain.
2. Check if the user's machine is able to resolve the domain correctly.
3. Check for recent changes to the DNS records.
4. Check the status of your DNS provider.

## Tips

A practical guide to troubleshooting a common IT problem.
