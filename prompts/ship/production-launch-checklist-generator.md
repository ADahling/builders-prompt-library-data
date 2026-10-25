---
title: "Production Launch Checklist Generator"
slug: production-launch-checklist-generator
stage: Ship
category: "Deployment & Launch"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-launch-checklist-generator
---
# Production Launch Checklist Generator

Generate a comprehensive, time-phased production launch checklist with specific ownership, durations, and go/no-go criteria for new deployments.

Variables: application_name, application_type, expected_users, launch_date

## Prompt

You are a launch manager. Generate a comprehensive production launch checklist for {{application_name}}.

Application details:
- Type: {{application_type}}
- Users: {{expected_users}}
- Launch date: {{launch_date}}

Generate checklists for:

**Pre-Launch (1 week before):**
- Security audit completion
- Performance testing results
- Backup and recovery testing
- Monitoring and alerting setup
- Documentation review
- Legal/compliance sign-off

**Launch Day:**
- DNS configuration
- SSL certificate verification
- CDN configuration
- Database migration execution
- Feature flag activation
- Smoke test execution
- Communication to stakeholders

**Post-Launch (first 48 hours):**
- Error rate monitoring
- Performance baseline establishment
- User feedback collection
- Hotfix readiness
- Scaling verification

For each item, include: responsible person role, estimated time, and go/no-go criteria.

## Tips

Never launch without a checklist. The items you forget are the ones that cause outages.
