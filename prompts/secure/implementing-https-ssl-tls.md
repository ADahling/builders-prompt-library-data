---
title: "Implementing HTTPS (SSL/TLS)"
slug: implementing-https-ssl-tls
stage: Secure
category: "Security Checklist"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-https-ssl-tls
---
# Implementing HTTPS (SSL/TLS)

Secure your website by obtaining a Let's Encrypt certificate and configuring a web server to enforce HTTPS and encrypt user communication.

Variables: domain_name, web_server_software, certificate_authority

## Prompt

You are a site reliability engineer (SRE) tasked with enabling HTTPS for a website that is currently served over HTTP. This is a critical step to protect user data in transit and improve the site's security posture. Your task is to obtain an SSL/TLS certificate and configure the web server to use it.

Context:
- The website domain is `{{domain_name}}`.
- The web server is `{{web_server_software}}`.
- You will use `{{certificate_authority}}` (e.g., Let's Encrypt) to obtain the certificate.

Provide:
1. An explanation of why HTTPS is important for all websites, not just those that handle sensitive data.
2. Step-by-step instructions on how to obtain a free SSL/TLS certificate from Let's Encrypt using a tool like Certbot.
3. A configuration example for your web server to enable HTTPS, including redirecting all HTTP traffic to HTTPS.

## Tips

An essential and practical guide for any website owner or administrator.
