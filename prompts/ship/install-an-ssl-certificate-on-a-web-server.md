---
title: "Install an SSL Certificate on a Web Server"
slug: install-an-ssl-certificate-on-a-web-server
stage: Ship
category: "Deployment & Launch"
grade: A+
score: 90
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/install-an-ssl-certificate-on-a-web-server
---
# Install an SSL Certificate on a Web Server

Secure a domain by installing an SSL certificate on Apache using Certbot with automated HTTPS redirection and validation.

Variables: ssl_provider, operating_system, domain_name

## Prompt

You are a web administrator. Your task is to install a free SSL certificate from {{ssl_provider}} on an Apache web server running on {{operating_system}}.

Instructions:
1. Use the Certbot client to obtain the SSL certificate for the domain `{{domain_name}}`.
2. Configure the Apache virtual host to use the new SSL certificate.
3. Ensure that HTTP traffic is automatically redirected to HTTPS.
4. Verify the SSL installation using an online SSL checker.

## Tips

An essential skill for web administrators, this prompt guides beginners through securing a website with SSL.
