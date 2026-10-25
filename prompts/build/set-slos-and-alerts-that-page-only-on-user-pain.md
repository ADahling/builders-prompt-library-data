---
title: "Set SLOs and alerts that page only on user pain"
slug: set-slos-and-alerts-that-page-only-on-user-pain
stage: Build
category: "DevOps & IaC"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-slos-and-alerts-that-page-only-on-user-pain
---
# Set SLOs and alerts that page only on user pain

Define service objectives and burn-rate alerts so pages map to real user impact, not noisy metrics.

Variables: service_name, critical_user_journey

## Prompt

You are a reliability engineer defining service objectives for a team drowning in alerts.

Context:
- The service: {{service_name}}
- The user journey that must not break: {{critical_user_journey}}

Your task is to define SLIs, SLOs, and alerting rules that page only when users are actually affected.

Steps:
1. Define the SLIs for the journey as ratios of good events over valid events. State the exact event definitions.
2. Propose an SLO target per SLI with the measurement window, and justify each target against user expectation rather than convenience.
3. Compute the resulting error budget and state what the team is permitted to do while it is intact.
4. Define multi-window burn-rate alerts: fast burn paging, slow burn ticketing, with thresholds and windows.
5. List the existing alerts this design replaces, and the ones to delete outright.
6. Define the review cadence and what happens when the budget is exhausted.

Constraints:
- No alert on a raw resource metric unless it is a leading indicator of journey failure.
- Every paging alert must name the user-visible symptom in its description.
- Do not set an SLO you cannot measure with data you already collect; flag the gaps instead.

Output format, in Markdown: an SLI/SLO table with columns SLI, definition, target, window; an alerts table with columns alert, condition, severity, response; then **Alerts to delete** and **Measurement gaps** as lists.

## Tips

If an alert cannot be tied to a user who is having a bad time, it belongs on a dashboard, not a pager.
