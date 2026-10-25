---
title: "Production Readiness: Security & Reliability Audit (OWASP)"
slug: production-readiness-security-reliability-audit-owasp
stage: Test
category: "Quality Audits"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-readiness-security-reliability-audit-owasp
---
# Production Readiness: Security & Reliability Audit (OWASP)

Perform a comprehensive security and reliability audit to identify vulnerabilities, prevent leaks, and harden your codebase for production.

## Prompt

Act as a paranoid but helpful security and reliability engineer. Analyze my entire codebase for vulnerabilities:

1. Input Validation (OWASP): Find all points where the app accepts user input (API endpoints, forms). Check for injection vulnerabilities (SQL, NoSQL, Command).
2. Cross-Site Scripting (XSS): Check if output to the user is properly sanitized or escaped.
3. Authentication/Authorization: Review how users are authenticated and permissions checked. Look for common flaws: missing auth on endpoints, broken access control, privilege escalation.
4. Insecure Dependencies: Scan package.json for dependencies with known CVEs. Suggest secure versions.
5. Secrets Management: Find any API keys, tokens, or credentials in source code or logs.
6. Error Information Leakage: Check that error messages don't reveal internal architecture, database schema, or stack traces.
7. Rate Limiting & Abuse Prevention: Identify endpoints vulnerable to brute force, credential stuffing, or resource exhaustion.
8. HTTPS & Transport Security: Verify all communications use TLS and security headers are set.
9. Reliability: Find single points of failure. What happens if the database is temporarily unavailable? If an external API times out?

For each finding: severity (Critical/High/Medium/Low), specific location, and exact code fix.

## Tips

Based on Richard Seroter's quality prompts + OWASP Top 10. This is the audit a professional security reviewer would do.
