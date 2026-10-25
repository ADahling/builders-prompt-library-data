---
title: "OWASP Top 10: Security Misconfiguration"
slug: owasp-top-10-security-misconfiguration
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/owasp-top-10-security-misconfiguration
---
# OWASP Top 10: Security Misconfiguration

Identify and remediate common web server vulnerabilities by applying hardened security configurations and establishing regular audit processes.

Variables: web_server_software, operating_system

## Prompt

You are a DevOps engineer responsible for securing a new web server. The server has been set up with default configurations, which may include security vulnerabilities. Your task is to identify and remediate common security misconfigurations.

Context:
- The web server is `{{web_server_software}}` (e.g., Nginx, Apache).
- The server is running on `{{operating_system}}`.

Provide:
1. A list of at least three common security misconfigurations for your chosen web server (e.g., default credentials, directory listing enabled, verbose error pages).
2. Step-by-step instructions on how to fix each of the identified misconfigurations.
3. A recommendation for a tool or a process to regularly scan for security misconfigurations.

## Tips

A practical prompt for anyone responsible for server administration and security.
