---
title: "DNS Security: DNSSEC"
slug: dns-security-dnssec
stage: Secure
category: "Security Checklist"
grade: A
score: 86
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/dns-security-dnssec
---
# DNS Security: DNSSEC

Develop and verify a comprehensive DNSSEC implementation plan to secure a specific domain against spoofing and cache poisoning attacks.

Variables: domain_name, dns_provider

## Prompt

You are a network administrator who is responsible for the DNS infrastructure of your organization. You want to implement DNSSEC to protect your domain from DNS spoofing and cache poisoning attacks. Your task is to create a plan for deploying DNSSEC for your domain.

Context:
- Your domain is `{{domain_name}}`.
- Your DNS is managed by `{{dns_provider}}` (e.g., AWS Route 53, Cloudflare, GoDaddy).

Provide:
1. An explanation of what DNSSEC is and how it works at a high level (i.e., the chain of trust).
2. A step-by-step guide on how to enable DNSSEC for your domain with your chosen DNS provider. This should include generating the necessary keys and creating the DS record.
3. A description of how to verify that DNSSEC has been correctly configured for your domain.

## Tips

An advanced prompt for network and system administrators on how to secure a critical part of the internet infrastructure.
