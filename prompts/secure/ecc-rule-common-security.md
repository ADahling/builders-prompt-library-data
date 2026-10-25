---
title: "ECC Rule: Common Security"
slug: ecc-rule-common-security
stage: Secure
category: "Security Review"
grade: C
score: 60
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/ecc-rule-common-security
---
# ECC Rule: Common Security

Review pre-commit security checks, secret handling, and critical issue response when preparing code changes or addressing vulnerabilities.

## Prompt

# Security Guidelines

## Mandatory Security Checks

Before ANY commit:
- [ ] No hardcoded secrets (API keys, passwords, tokens)
- [ ] All user inputs validated
- [ ] SQL injection prevention (parameterized queries)
- [ ] XSS prevention (sanitized HTML)
- [ ] CSRF protection enabled
- [ ] Authentication/authorization verified
- [ ] Rate limiting on all endpoints
- [ ] Error messages don't leak sensitive data

## Secret Management

- NEVER hardcode secrets in source code
- ALWAYS use environment variables or a secret manager
- Validate that required secrets are present at startup
- Rotate any secrets that may have been exposed

## Security Response Protocol

If security issue found:
1. STOP immediately
2. Use **security-reviewer** agent
3. Fix CRITICAL issues before continuing
4. Rotate any exposed secrets
5. Review entire codebase for similar issues

## Tips

Source: Everything Claude Code (ECC) — Rule: common/security
