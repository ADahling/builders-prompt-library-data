---
title: "Incident Postmortem Template"
slug: incident-postmortem-template
stage: Ship
category: "Monitoring & Observability"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/incident-postmortem-template
---
# Incident Postmortem Template

Write a blameless incident postmortem with impact metrics, a leadership summary, an event timeline, and systemic root cause analysis.

Variables: incident_title, 1-4, start_time, end_time, total_minutes, users_affected, revenue_impact, how_detected, minutes, name, Factual description of the failure chain. Not "human error" — dig deeper into systemic causes., answer, answer — this should reveal a systemic cause, prevent recurrence, date, ticket, improve detection, systemic improvement, percentage of users / services affected

## Prompt

# Blameless Incident Postmortem

Write a blameless postmortem for this incident:
- Incident: [brief description]
- Duration: [start time — end time]
- Impact: [who was affected, how]
- Severity: [SEV-1 / SEV-2 / SEV-3 / SEV-4]

## Incident Summary
| Field | Value |
|-------|-------|
| Title | {{incident_title}} |
| Severity | SEV-{{1-4}} |
| Duration | {{start_time}} — {{end_time}} ({{total_minutes}} min) |
| Impact | {{users_affected}} users, {{revenue_impact}} revenue impact |
| Detection | {{how_detected}} (monitoring / customer report / internal) |
| Time to Detect (TTD) | {{minutes}} |
| Time to Mitigate (TTM) | {{minutes}} |
| Incident Commander | {{name}} |

## Executive Summary
2-3 sentences for leadership: what happened, how long, what we did.

## Timeline
| Time (UTC) | Event | Actor |
|------------|-------|-------|
| HH:MM | First error detected by monitoring | System |
| HH:MM | Alert fired, on-call paged | PagerDuty / monitoring |
| HH:MM | IC acknowledged, investigation began | On-call engineer |
| HH:MM | Root cause identified | Team |
| HH:MM | Mitigation applied | Engineer |
| HH:MM | Full recovery confirmed | IC |

## Root Cause Analysis
### What Actually Broke
{{Factual description of the failure chain. Not "human error" — dig deeper into systemic causes.}}

### 5 Whys
1. Why did the outage occur? → {{answer}}
2. Why did that happen? → {{answer}}
3. Why? → {{answer}}
4. Why? → {{answer}}
5. Why? → {{answer — this should reveal a systemic cause}}

### Contributing Factors
- [ ] Code change (link to PR/commit)
- [ ] Configuration change
- [ ] Infrastructure failure
- [ ] Dependency failure
- [ ] Capacity/scaling issue
- [ ] Process gap (missing runbook, unclear ownership)
- [ ] Communication failure
- [ ] Inadequate testing / monitoring

## Response Assessment
### What Went Well
- Things that helped during detection and response

### What Went Poorly
- Things that hindered detection or resolution

### What Was Lucky
- Things that could have been worse

## Action Items
| Priority | Action | Owner | Due Date | Tracking |
|----------|--------|-------|----------|----------|
| P0 — Immediate (this week) | {{prevent recurrence}} | {{name}} | {{date}} | {{ticket}} |
| P1 — Short-term (this month) | {{improve detection}} | {{name}} | {{date}} | {{ticket}} |
| P2 — Long-term (this quarter) | {{systemic improvement}} | {{name}} | {{date}} | {{ticket}} |

## Metrics
- **MTTD** (Mean Time to Detect): {{minutes}}
- **MTTA** (Mean Time to Acknowledge): {{minutes}}
- **MTTR** (Mean Time to Resolve): {{minutes}}
- **Blast radius**: {{percentage of users / services affected}}

## Blamelessness Statement
This postmortem focuses on systems, processes, and tooling — not individuals. The goal is to learn and improve so this class of incident cannot recur.

Tone: Blameless, factual, focused on systems not people.

## Tips

The postmortem is more valuable than the fix if it prevents future incidents. Consolidates timeline, 5-Whys root cause analysis, contributing factors checklist, prioritized action items, and incident metrics into one comprehensive template.
