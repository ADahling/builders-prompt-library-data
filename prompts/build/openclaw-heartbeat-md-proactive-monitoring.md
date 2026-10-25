---
title: "OpenClaw HEARTBEAT.md \u2014 Proactive Monitoring"
slug: openclaw-heartbeat-md-proactive-monitoring
stage: Build
category: "OpenClaw"
grade: C
score: 67
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-heartbeat-md-proactive-monitoring
---
# OpenClaw HEARTBEAT.md — Proactive Monitoring

HEARTBEAT.md — Proactive Agent Triggers This file turns your agent from reactive to proactive.

## Prompt

# HEARTBEAT.md — Proactive Agent Triggers

*This file turns your agent from reactive to proactive. Define what it should check on a schedule.*

## Every 30 Minutes (During Work Hours)
- [ ] Check email inbox for urgent messages (DRAFT-ONLY mode — never send)
- [ ] Scan Slack for @mentions or DMs requiring response
- [ ] Check calendar for meetings starting in the next 45 minutes
- [ ] Monitor CI/CD pipeline status for active PRs
- [ ] Check server health dashboards for anomalies

## Every Hour
- [ ] Review task list for approaching deadlines
- [ ] Check for new GitHub notifications (PRs, issues, reviews)
- [ ] Scan news feeds for breaking stories in tracked topics
- [ ] Update daily memory file with observations

## Every 4 Hours
- [ ] Generate status summary of all monitored systems
- [ ] Review and categorize unread emails
- [ ] Check infrastructure costs against daily budget
- [ ] Update MEMORY.md with curated insights

## Daily (Scheduled)
- **6:00 AM:** Pre-brief — check calendar, prepare meeting contexts, pull CRM data on attendees
- **7:00 AM:** Morning briefing — news, calendar, tasks, overnight alerts
- **12:00 PM:** Midday check-in — progress update, afternoon priority suggestions
- **6:00 PM:** End-of-day summary — completed tasks, open items, tomorrow's priorities
- **10:00 PM:** Overnight prep — queue non-urgent analyses for overnight processing

## Weekly (Scheduled)
- **Sunday 8:00 PM:** Week-ahead preview — major meetings, deadlines, travel
- **Friday 5:00 PM:** Week-in-review — accomplishments, metrics, learnings
- **Wednesday 9:00 AM:** Technical debt review — scan repos for issues

## Alert Conditions (Immediate — Override Quiet Hours)
- Security incident detected
- Server downtime or error rate spike > 5%
- Deployment failure
- Urgent email from VIP contacts list
- Calendar conflict detected for tomorrow

## Severity Tags
- **[URGENT]** — Requires immediate attention, overrides quiet hours
- **[HEADS UP]** — Important but not time-critical, can wait for next check
- **[FYI]** — Informational, include in next briefing

## Tips

HEARTBEAT.md is the game-changer that turns an agent from reactive to proactive. Customize the schedules and checks to match your workflow. Community consensus: this is the most underrated OpenClaw file.
