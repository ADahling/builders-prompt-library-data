---
title: "CI/CD Pipeline Generator (GitHub Actions)"
slug: ci-cd-pipeline-generator-github-actions
stage: Build
category: "DevOps & IaC"
grade: B
score: 75
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ci-cd-pipeline-generator-github-actions
---
# CI/CD Pipeline Generator (GitHub Actions)

Get a commented GitHub Actions workflow for your project with linting, tests, builds, security checks, staged deploys, and rollback.

## Prompt

Generate a complete GitHub Actions CI/CD pipeline for my [describe project]:

1. LINT & FORMAT:
   - ESLint with strict TypeScript rules
   - Prettier formatting check
   - Fail fast on lint errors

2. TEST:
   - Unit tests (Vitest / Jest)
   - Integration tests
   - E2E tests (Playwright / Cypress)
   - Coverage threshold (e.g., 80%)

3. BUILD:
   - TypeScript compilation (tsc --noEmit)
   - Vite / Next.js build
   - Bundle size check (fail if > threshold)

4. SECURITY:
   - npm audit for vulnerabilities
   - Secret scanning
   - SAST (static analysis)

5. DEPLOY:
   - Staging deploy on PR merge to develop
   - Production deploy on release tag
   - Rollback strategy on failure
   - Slack/Discord notification on deploy

6. ENVIRONMENT:
   - Environment secrets management
   - Branch protection rules
   - Required status checks

Provide the complete .github/workflows/ci.yml file with comments explaining each step.

## Tips

Adapted from Firefly.ai's battle-tested DevOps prompts. Source: firefly.ai/academy/master-prompt-engineering-top-10
