---
title: "Generate a Runbook for a Production Outage"
slug: generate-a-runbook-for-a-production-outage
stage: Design
category: "Documentation"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-runbook-for-a-production-outage
---
# Generate a Runbook for a Production Outage

Create a comprehensive SRE runbook in Markdown to standardize incident response, diagnostic procedures, and service restoration workflows.

Variables: service_name, dependency_1, dependency_2, dashboard_url

## Prompt

You are a Site Reliability Engineer (SRE) responsible for creating a runbook to handle a critical production outage: the {{service_name}} service is down. A well-defined runbook is essential for a quick and effective response to minimize downtime and impact on users.

Your task is to generate a detailed runbook in Markdown format that provides step-by-step instructions for on-call engineers. The runbook should include the following sections:

*   **Alert:** The specific alert that triggers this runbook.
*   **Severity:** The severity level of the outage (e.g., SEV-1, SEV-2).
*   **Immediate Actions:** A checklist of the first steps to take, such as acknowledging the alert, starting a war room, and notifying stakeholders.
*   **Diagnosis:** A series of diagnostic steps to identify the root cause of the outage. This should include commands to run, logs to check, and metrics to analyze.
*   **Mitigation:** Step-by-step instructions on how to mitigate the issue and restore the service. This may include rolling back a recent deployment, restarting a service, or failing over to a backup system.
*   **Post-Mortem:** Instructions on what information to collect for the post-mortem analysis, such as a timeline of events, key metrics, and customer impact.

Here is some information about the service:

*   **Service Name:** {{service_name}}
*   **Key Dependencies:** {{dependency_1}}, {{dependency_2}}
*   **Monitoring Dashboard:** {{dashboard_url}}

Generate the complete runbook. The instructions should be clear, unambiguous, and easy to follow under pressure.
