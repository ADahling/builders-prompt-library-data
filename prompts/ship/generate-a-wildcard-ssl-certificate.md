---
title: "Generate a Wildcard SSL Certificate"
slug: generate-a-wildcard-ssl-certificate
stage: Ship
category: "Deployment & Launch"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-wildcard-ssl-certificate
---
# Generate a Wildcard SSL Certificate

Generate a wildcard SSL certificate using Certbot and DNS-01 challenges to secure all subdomains under a single domain.

Variables: domain_name, ssl_provider

## Prompt

You are a web administrator. You need to secure multiple subdomains of `{{domain_name}}`. Your task is to generate a wildcard SSL certificate, `*.{{domain_name}}`, using `{{ssl_provider}}`.

Instructions:
1. Use Certbot to request a wildcard certificate.
2. You will need to use the DNS-01 challenge method, which requires you to create a `TXT` record in your DNS to prove you own the domain.
3. Certbot can often automate this process if your DNS provider has an API.
4. Install the wildcard certificate on your web server to secure all your subdomains.

## Tips

A convenient way to secure an unlimited number of subdomains.
