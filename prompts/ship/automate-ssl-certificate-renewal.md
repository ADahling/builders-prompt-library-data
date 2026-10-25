---
title: "Automate SSL Certificate Renewal"
slug: automate-ssl-certificate-renewal
stage: Ship
category: "Deployment & Launch"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/automate-ssl-certificate-renewal
---
# Automate SSL Certificate Renewal

Automate SSL certificate issuance and scheduled renewal for web servers using Certbot to ensure continuous HTTPS encryption.

Variables: ssl_provider, web_server_name

## Prompt

You are a system administrator. Your SSL certificate is about to expire. Your task is to automate the renewal process using `{{ssl_provider}}`'s client, Certbot.

Instructions:
1. Install Certbot on your web server.
2. Run Certbot to obtain and install the certificate.
3. Certbot should automatically configure your web server (`{{web_server_name}}`) to use the certificate.
4. Set up a cron job or systemd timer to run `certbot renew` periodically to automatically renew the certificate before it expires.

## Tips

A set-it-and-forget-it approach to SSL certificate management.
