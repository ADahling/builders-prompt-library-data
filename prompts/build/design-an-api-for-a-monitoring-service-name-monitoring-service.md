---
title: "Design an API for a Monitoring Service"
slug: design-an-api-for-a-monitoring-service-name-monitoring-service
stage: Build
category: "API Design"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-monitoring-service-name-monitoring-service
---
# Design an API for a Monitoring Service

Get a monitoring API design for ingesting metrics and logs, querying and visualizing data, and configuring rule-based alerts, with endpoint formats.

Variables: monitoring_service_name

## Prompt

I am building a monitoring service called {{monitoring_service_name}} that will collect metrics and logs from other applications. I need to design the API for it.

Your task is to design the core API for the service.

**Instructions:**
1.  **Data Ingestion:** Design an API for ingesting metrics and logs from various sources.
2.  **Data Querying:** Design an API for querying and visualizing the collected data.
3.  **Alerting:** Design an API for setting up alerts based on predefined rules.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoint, including the HTTP method, URI, and request/response format.
