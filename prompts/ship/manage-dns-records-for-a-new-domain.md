---
title: "Manage DNS Records for a New Domain"
slug: manage-dns-records-for-a-new-domain
stage: Ship
category: "Deployment & Launch"
grade: B
score: 75
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/manage-dns-records-for-a-new-domain
---
# Manage DNS Records for a New Domain

Configure a domain's DNS infrastucture by setting up A, CNAME, and MX records via a specified provider to ensure proper routing and mail delivery.

Variables: domain_name, dns_provider, ip_address, mail_server

## Prompt

You are a system administrator. Your task is to manage the DNS records for a new domain, `{{domain_name}}`, using {{dns_provider}}.

Instructions:
1. Add an `A` record to point the root domain to the IP address `{{ip_address}}`.
2. Create a `CNAME` record for `www` to point to the root domain.
3. Add an `MX` record for email handling, pointing to `{{mail_server}}`.
4. Verify that the DNS records have propagated correctly.

## Tips

A basic prompt for those learning about DNS management and configuration.
