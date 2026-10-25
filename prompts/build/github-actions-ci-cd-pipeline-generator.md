---
title: "GitHub Actions CI/CD Pipeline Generator"
slug: github-actions-ci-cd-pipeline-generator
stage: Build
category: "DevOps & IaC"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/github-actions-ci-cd-pipeline-generator
---
# GitHub Actions CI/CD Pipeline Generator

Generate a production-ready GitHub Actions CI/CD suite with automated testing, multi-stage deployment, security scanning, and rollbacks.

Variables: project_name, language, framework, deployment_target, database

## Prompt

You are a DevOps engineer. Generate a production-grade GitHub Actions CI/CD pipeline for {{project_name}}.

Project details:
- Language: {{language}}
- Framework: {{framework}}
- Deployment target: {{deployment_target}}
- Database: {{database}}

Generate workflows for:
1. **CI Pipeline** (on PR): Lint, type check, unit tests, integration tests, build, security scan
2. **CD Pipeline** (on merge to main): Build, deploy to staging, run E2E tests, deploy to production
3. **Dependency Updates**: Dependabot config with auto-merge for patch updates
4. **Release Management**: Semantic versioning, changelog generation, GitHub releases
5. **Environment Management**: Staging and production environment secrets
6. **Caching Strategy**: Node modules, build artifacts, Docker layers
7. **Notifications**: Slack notifications for failures and deployments
8. **Rollback**: Manual rollback workflow trigger

Include:
- Proper job dependencies and parallelization
- Matrix builds for multiple Node versions
- Artifact upload/download between jobs
- Concurrency controls to prevent duplicate deployments

## Tips

A good CI/CD pipeline catches 90% of issues before they reach production.
