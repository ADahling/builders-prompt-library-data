---
title: "CORS Configuration for a Public API"
slug: cors-configuration-for-a-public-api
stage: Secure
category: "Security Checklist"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cors-configuration-for-a-public-api
---
# CORS Configuration for a Public API

Implement a secure CORS policy for a public API using a specific framework to restrict cross-origin access to an authorized web domain.

Variables: api_domain, webapp_domain, api_framework

## Prompt

You are deploying a new public API and need to configure Cross-Origin Resource Sharing (CORS) to allow access from specific domains. The API should be accessible from your company's official web application but not from any other domain. Your task is to implement a secure CORS policy.

Context:
- The API is hosted at `{{api_domain}}`.
- The web application that needs access is hosted at `{{webapp_domain}}`.
- The API is built with `{{api_framework}}`.

Provide:
1. An explanation of what CORS is and why it is necessary for web security.
2. A code example showing how to configure CORS to allow requests only from `{{webapp_domain}}`.
3. A brief discussion of the security implications of using a wildcard (`*`) in your CORS configuration.

## Tips

A practical guide to configuring CORS, a common requirement for modern web applications.
