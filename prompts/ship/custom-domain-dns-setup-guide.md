---
title: "Custom Domain & DNS Setup Guide"
slug: custom-domain-dns-setup-guide
stage: Ship
category: "Deployment & Launch"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/custom-domain-dns-setup-guide
---
# Custom Domain & DNS Setup Guide

Get a custom domain setup guide for your hosting platform, covering DNS records, HTTPS, redirects, email authentication, and verification.

## Prompt

Set up a custom domain for my [describe app / hosting platform]:

1. Domain Purchase: Where to buy (Namecheap, Cloudflare, Google Domains). What TLD to choose (.com, .app, .dev, .io) and why.
2. DNS Configuration:
   - A record pointing to hosting IP
   - CNAME for www subdomain
   - MX records if using custom email
   - TXT records for domain verification (Google, Stripe, etc.)
3. SSL/TLS: How to set up HTTPS. Auto-provisioning via Let's Encrypt or hosting provider.
4. Redirects:
   - www to non-www (or vice versa) — pick one and redirect the other
   - HTTP to HTTPS redirect
   - Old URLs to new URLs (if migrating)
5. Email Setup: Configure SPF, DKIM, DMARC records for email deliverability.
6. Subdomains: app.domain.com, api.domain.com, docs.domain.com — when and how.
7. Verification: How to test DNS propagation. Tools: dig, nslookup, whatsmydns.net.
8. Common Mistakes: TTL too high during migration, missing www redirect, forgetting email DNS records.

## Tips

DNS misconfiguration is the #1 cause of launch-day delays. Set this up a week before launch.
