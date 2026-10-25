---
title: "Data Quality Framework Design"
slug: data-quality-framework-design
stage: Build
category: "Modern Data Stack"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/data-quality-framework-design
---
# Data Quality Framework Design

Architect a robust, end-to-end data quality framework featuring automated validation, alerting strategies, and remediation workflows.

Variables: data_pipeline_name, data_sources, data_volume, freshness_sla, downstream_consumers

## Prompt

You are a data quality engineer. Design a comprehensive data quality framework for {{data_pipeline_name}}.

Pipeline details:
- Sources: {{data_sources}}
- Volume: {{data_volume}} records/day
- SLA: {{freshness_sla}}
- Critical consumers: {{downstream_consumers}}

Design a framework covering:
1. **Quality Dimensions**: Completeness, accuracy, consistency, timeliness, uniqueness, validity
2. **Check Types**: Schema validation, statistical anomaly detection, business rule validation, cross-source reconciliation
3. **Implementation**: Great Expectations, dbt tests, or custom checks? Show code examples
4. **Alerting**: When to alert, who to alert, escalation paths
5. **Remediation**: Quarantine bad data, auto-fix known issues, manual review queue
6. **Monitoring Dashboard**: Key metrics to track over time
7. **SLA Tracking**: How to measure and report on data freshness and quality SLAs
8. **Root Cause Analysis**: Playbook for investigating quality issues

## Tips

Data quality is the #1 complaint from business users. This framework prevents 'garbage in, garbage out'.
