---
title: "Clickjacking Attack Prevention"
slug: clickjacking-attack-prevention
stage: Secure
category: "Security Checklist"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/clickjacking-attack-prevention
---
# Clickjacking Attack Prevention

Secure your website against clickjacking by implementing X-Frame-Options headers to control iframe embedding permissions.

Variables: website_domain

## Prompt

You are a web developer who has learned about clickjacking attacks. You want to protect your website from this type of attack. Your task is to implement the `X-Frame-Options` header to prevent your site from being loaded in an iframe on other sites.

Context:
- Your website is `{{website_domain}}`.
- You have access to the web server configuration or can add headers in your application code.

Provide:
1. An explanation of what a clickjacking attack is and how it works.
2. The different values for the `X-Frame-Options` header (`DENY`, `SAMEORIGIN`) and what they mean.
3. A code example or configuration snippet showing how to add the `X-Frame-Options` header to your website.

## Tips

A simple but effective defense against a common web attack.
