---
title: "Zero-Downtime Deployment Strategy"
slug: zero-downtime-deployment-strategy
stage: Ship
category: "Deployment & Launch"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/zero-downtime-deployment-strategy
---
# Zero-Downtime Deployment Strategy

Design and document a comprehensive zero-downtime deployment architecture, covering migration patterns, traffic shifting, and rollback logic.

Variables: application_name, infrastructure, database, requests_per_second, deployment_frequency

## Prompt

You are a DevOps architect. Design a zero-downtime deployment strategy for {{application_name}}.

Current setup:
- Infrastructure: {{infrastructure}}
- Database: {{database}}
- Traffic: {{requests_per_second}} req/s
- Deployment frequency: {{deployment_frequency}}

Design:
1. **Deployment Method**: Blue-green, canary, or rolling? Justify your choice
2. **Database Migrations**: How to run migrations without downtime (expand-contract pattern)
3. **Feature Flags**: How to decouple deployment from release
4. **Health Checks**: Readiness and liveness probes configuration
5. **Rollback Strategy**: Automated rollback triggers and manual rollback procedure
6. **Traffic Management**: How to gradually shift traffic to new version
7. **Monitoring**: Key metrics to watch during deployment
8. **Runbook**: Step-by-step deployment procedure with decision points
9. **Post-Deployment Verification**: Smoke tests and synthetic monitoring

## Tips

Zero-downtime deployment is table stakes for production services. The database migration strategy is usually the hardest part.
