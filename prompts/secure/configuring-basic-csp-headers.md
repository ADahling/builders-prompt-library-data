---
title: "Configuring Basic CSP Headers"
slug: configuring-basic-csp-headers
stage: Secure
category: "Security Checklist"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/configuring-basic-csp-headers
---
# Configuring Basic CSP Headers

Get a basic CSP header and implementation steps for an app without a policy, allowing its own domain and Google Analytics as content sources.

Variables: app_type, app_domain

## Prompt

You need to improve the security of a web application by implementing a Content Security Policy (CSP). The application currently has no CSP, leaving it more vulnerable to XSS and other injection attacks. Your goal is to create a basic CSP that restricts the sources of content.

Context:
- The application is a {{app_type}} hosted at {{app_domain}}.
- The application loads scripts from its own domain and from Google Analytics.

Provide:
1. An explanation of what a Content Security Policy is and how it helps prevent attacks.
2. A sample CSP header that allows content from the application's own domain and from Google Analytics.
3. Instructions on how to implement the CSP header in a popular web server like Nginx or Apache, or directly in your application code.

## Tips

A great starting point for learning about and implementing CSPs.
