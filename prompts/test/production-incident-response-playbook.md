---
title: "Production Incident Response Playbook"
slug: production-incident-response-playbook
stage: Test
category: "Critical Bugs"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-incident-response-playbook
---
# Production Incident Response Playbook

Generate a comprehensive, system-specific incident response playbook to accelerate diagnosis and mitigation during critical production outages.

Variables: incident_type, application_name, architecture_description, sla_target, on_call_structure, logging_tool, monitoring_tool, database_type, infrastructure_type

## Prompt

You are an SRE lead. Create a production incident response playbook for {{incident_type}} in {{application_name}}.

System context:
- Architecture: {{architecture_description}}
- SLA: {{sla_target}}
- On-call rotation: {{on_call_structure}}

Playbook sections:
1. **Detection**: How is this incident type detected? (alerts, user reports, monitoring)
2. **Severity Classification**: Criteria for P1/P2/P3/P4
3. **Immediate Response** (first 5 minutes): Who to page, what to check first
4. **Diagnosis Checklist**: Step-by-step investigation procedure with specific commands and queries
5. **Mitigation Options**: Ranked by speed vs risk (restart, rollback, feature flag, scale up, failover)
6. **Communication Template**: Status page update, Slack message, customer email
7. **Resolution Verification**: How to confirm the incident is resolved
8. **Post-Incident**: Blameless postmortem template, action items tracking

Include specific commands for:
- Checking logs: {{logging_tool}}
- Checking metrics: {{monitoring_tool}}
- Checking database: {{database_type}}
- Checking infrastructure: {{infrastructure_type}}

## Tips

Write playbooks BEFORE incidents happen. During an outage, you won't have time to think clearly.
