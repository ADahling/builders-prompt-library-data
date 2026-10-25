---
title: "Environment Configuration & Secrets Management"
slug: environment-configuration-secrets-management
stage: Ship
category: "Deployment & Launch"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/environment-configuration-secrets-management
---
# Environment Configuration & Secrets Management

Set up app environment tiers, secret storage rules, rotation plans, startup validation, and documentation for required variables.

## Prompt

Set up proper environment configuration for my [describe app]:

1. Environment Tiers:
   - Development (local): .env.local with test API keys, local database URL
   - Staging: Mirror of production with test data, test payment keys
   - Production: Real API keys, production database, live payments

2. Secret Categories:
   | Type | Example | Where to Store |
   |------|---------|----------------|
   | Public | Supabase anon key, GA tracking ID | .env (committed) |
   | Private | Stripe secret key, SMTP password | Platform secrets (never in code) |
   | Generated | JWT signing key, encryption key | Platform secrets, auto-rotated |

3. Configuration Checklist:
   - [ ] No secrets in source code or Git history
   - [ ] .env.example file with all required variables (no values)
   - [ ] Different API keys per environment (never share prod keys in dev)
   - [ ] Secrets rotation plan (quarterly minimum)
   - [ ] Access audit: who has access to production secrets?

4. Validation: On app startup, verify all required env vars are set. Fail fast with clear error message if missing.

5. Documentation: Table of every environment variable with name, description, required/optional, example value, and which environments need it.

## Tips

Leaked API keys are the most common security incident. Get this right from day one.
