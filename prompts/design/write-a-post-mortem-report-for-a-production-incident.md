---
title: "Write a Post-Mortem Report for a Production Incident"
slug: write-a-post-mortem-report-for-a-production-incident
stage: Design
category: "Documentation"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-post-mortem-report-for-a-production-incident
---
# Write a Post-Mortem Report for a Production Incident

Generate a blameless post-mortem report in Markdown to document root causes, timelines, and SMART action items after a production incident.

Variables: incident_description, incident_impact, root_cause

## Prompt

You are the incident commander for a recent production incident. Now that the incident has been resolved, you need to write a post-mortem report to analyze the root cause, document the impact, and identify follow-up actions to prevent similar incidents in the future.

Your task is to generate a comprehensive post-mortem report that includes the following sections:

*   **Summary:** A brief overview of the incident, including what happened, the impact, and the duration.
*   **Timeline:** A detailed timeline of events, from the initial alert to the resolution of the incident.
*   **Root Cause Analysis:** A thorough analysis of the root cause of the incident.
*   **Impact Analysis:** An assessment of the impact of the incident on customers, business operations, and system performance.
*   **Lessons Learned:** A discussion of what went well and what could be improved in the incident response process.
*   **Action Items:** A list of specific, measurable, achievable, relevant, and time-bound (SMART) action items to address the root cause and prevent recurrence.

Here is some information about the incident:

*   **Incident:** {{incident_description}}
*   **Impact:** {{incident_impact}}
*   **Root Cause:** {{root_cause}}

Generate the complete post-mortem report in Markdown format. The report should be blameless and focus on learning and improvement.
