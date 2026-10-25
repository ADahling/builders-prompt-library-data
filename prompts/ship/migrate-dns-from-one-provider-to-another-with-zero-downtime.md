---
title: "Migrate DNS from one Provider to Another with Zero Downtime"
slug: migrate-dns-from-one-provider-to-another-with-zero-downtime
stage: Ship
category: "Deployment & Launch"
grade: C
score: 61
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/migrate-dns-from-one-provider-to-another-with-zero-downtime
---
# Migrate DNS from one Provider to Another with Zero Downtime

Execute a seamless DNS transition between providers by following a structured migration workflow to prevent service interruptions.

Variables: domain_name, new_dns_provider

## Prompt

You are a system administrator. Your task is to migrate the DNS for a live domain, `{{domain_name}}`, from your current provider to a new provider, `{{new_dns_provider}}`, with zero downtime.

Instructions:
1. Export all your current DNS records.
2. Import them into the new DNS provider.
3. Lower the TTL on your records at your current provider.
4. Change the name servers for your domain at your domain registrar to point to the new provider.
5. Monitor the migration to ensure it completes successfully.

## Tips

A delicate operation that requires careful planning and execution.
