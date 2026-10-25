---
title: "Define SLOs for a Web Application"
slug: define-slos-for-a-web-application
stage: Ship
category: "Monitoring & Observability"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/define-slos-for-a-web-application
---
# Define SLOs for a Web Application

Establish comprehensive Service Level Objectives for a web application by defining reliability targets, monitoring strategies, and review plans.

Variables: app_name, tech_stack

## Prompt

You are tasked with defining Service Level Objectives (SLOs) for a web application called {{app_name}} that runs on a {{tech_stack}} stack. Consider the following requirements: the application should have a monthly availability of 99.9%, a maximum response time of 300ms for 95% of requests, and an error rate below 0.1% for server-side operations. Outline the SLOs in detail, including the rationale for these targets and how they align with user expectations and business goals. Additionally, specify how these SLOs can be measured and monitored using tools like Prometheus, Grafana, or New Relic. Provide a clear plan for regular review and adjustment of these SLOs to ensure they remain aligned with evolving business needs.

## Tips

Use this prompt to establish clear and measurable SLOs for a web-based project.
