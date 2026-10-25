---
title: "API Security Hardening Checklist"
slug: api-security-hardening-checklist
stage: Secure
category: "Security Checklist"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-security-hardening-checklist
---
# API Security Hardening Checklist

Conduct a comprehensive security audit of an API to identify vulnerabilities and provide severity-rated remediations with proof-of-concept code.

Variables: api_name, framework, auth_method, number_of_endpoints, data_classification

## Prompt

You are an API security specialist. Perform a comprehensive security audit of the {{api_name}} API.

API details:
- Framework: {{framework}}
- Authentication: {{auth_method}}
- Endpoints: {{number_of_endpoints}}
- Data sensitivity: {{data_classification}}

Audit the following areas:

1. **Authentication & Authorization**: Token validation, session management, role-based access
2. **Input Validation**: SQL injection, XSS, command injection, path traversal
3. **Rate Limiting**: Per-user, per-IP, per-endpoint limits
4. **Data Exposure**: Over-fetching, sensitive data in responses, error message leakage
5. **Transport Security**: TLS configuration, HSTS, certificate pinning
6. **CORS Configuration**: Allowed origins, methods, headers
7. **Logging & Monitoring**: Security events to log, anomaly detection
8. **Dependency Security**: Known vulnerabilities in dependencies

For each finding, provide:
- Severity (Critical/High/Medium/Low)
- The vulnerability
- Proof of concept
- Remediation code
- Verification test

## Tips

Run this before every API goes to production. Covers OWASP API Security Top 10.
