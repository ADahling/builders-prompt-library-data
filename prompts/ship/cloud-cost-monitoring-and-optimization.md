---
title: "Cloud Cost Monitoring and Optimization"
slug: cloud-cost-monitoring-and-optimization
stage: Ship
category: "Monitoring & Observability"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cloud-cost-monitoring-and-optimization
---
# Cloud Cost Monitoring and Optimization

Get a cloud spending report for your project with monthly costs, expensive resources, unexpected charges, and suggested optimization actions.

Variables: project_name, cloud_provider, monthly_expenditure, high_cost_resources, savings_opportunities, optimization_actions

## Prompt

Monitor and optimize cloud costs for the {{project_name}} project hosted on {{cloud_provider}}. Start by analyzing the current spending patterns using the provider's billing dashboard. Identify services or resources that incur the highest costs and investigate any unexpected charges. Develop a strategy to optimize spending, such as rightsizing instances, utilizing reserved instances, or removing unused resources. Your report should detail:

- Current monthly expenditure: {{monthly_expenditure}}
- High-cost resources: {{high_cost_resources}}
- Potential savings opportunities: {{savings_opportunities}}
- Suggested optimization actions: {{optimization_actions}}

The goal is to provide actionable insights that can lead to significant cost savings without compromising performance.

## Tips

Intermediate task focusing on cloud cost management.
