---
title: "Environment Variable Security Audit"
slug: environment-variable-security-audit
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/environment-variable-security-audit
---
# Environment Variable Security Audit

Identify security vulnerabilities in environment variable management to prevent secret leaks and implement professional rotation and encryption standards.

Variables: project_name, env_management_description

## Prompt

You are a DevSecOps engineer. Audit the environment variable management for {{project_name}}.

Current setup:
- {{env_management_description}}

Check for:
1. **Exposed Secrets**: Are any API keys, passwords, or tokens committed to git?
2. **Client-Side Leaks**: Are any server-only secrets exposed to the browser (VITE_, NEXT_PUBLIC_, REACT_APP_ prefixes)?
3. **Default Values**: Are there hardcoded fallback values that could be exploited?
4. **Rotation Policy**: How often are secrets rotated? Is there a process?
5. **Access Control**: Who has access to production secrets?
6. **Encryption at Rest**: Are secrets encrypted in CI/CD and hosting platforms?
7. **.env File Management**: Are .env files in .gitignore? Are there .env.example files?

Provide:
- A categorized list of all environment variables (public vs secret)
- Risk assessment for each
- Recommended secret management solution (Vault, AWS Secrets Manager, etc.)
- Migration plan from current setup

## Tips

The #1 cause of security breaches in vibe-coded apps is exposed environment variables.
