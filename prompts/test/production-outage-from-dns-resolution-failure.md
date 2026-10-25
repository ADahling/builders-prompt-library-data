---
title: "Production Outage from DNS Resolution Failure"
slug: production-outage-from-dns-resolution-failure
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-outage-from-dns-resolution-failure
---
# Production Outage from DNS Resolution Failure

Diagnose and resolve website accessibility issues caused by DNS failures using systematic troubleshooting commands and mitigation strategies.

## Prompt

You are a network engineer. Your company’s website is inaccessible to a large number of users. You suspect a DNS issue. Your task is to diagnose and resolve the DNS failure.

Context:
- The website is served through a CDN, and its DNS is managed by a major DNS provider.
- Users are reporting that the domain name is not resolving to an IP address.
- You have access to DNS diagnostic tools.

Provide:
1. A list of commands (like `dig`, `nslookup`, `traceroute`) to diagnose the DNS problem from an external perspective.
2. A checklist of things to investigate within your DNS provider’s control panel, such as misconfigured DNS records (A, CNAME, NS) or a service outage on their end.
3. A plan for communicating with your DNS provider’s support and a short-term mitigation strategy, such as lowering DNS TTLs in preparation for a change.

## Tips

A critical infrastructure problem that requires network troubleshooting skills.
