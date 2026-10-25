---
title: "OpenClaw: OKR Tracker & Decision Log"
slug: openclaw-okr-tracker-decision-log
stage: Build
category: "OpenClaw"
grade: A
score: 88
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-okr-tracker-decision-log
---
# OpenClaw: OKR Tracker & Decision Log

Set up weekly OKR progress reports and a decision log with context, owners, review dates, and reminders for tracking goals and outcomes.

Variables: number, Description, description, current, target, %, 🟢 On Track / 🟡 At Risk / 🔴 Behind, progress made, if any, X of Y, KR most behind, specific action, KR closest to completion, Quarter, Date, Decision Title, Why this decision was needed, What was decided, Options not chosen and why, Who is responsible for execution, When to evaluate if decision was correct, Filled in at review date

## Prompt

# OKR Tracker & Decision Log — OpenClaw Founder Automation

## OKR Tracking (Weekly, Friday 4 PM)
Pull progress from task management tools (Asana/Linear/Notion):

```
📊 OKR PROGRESS — Week {{number}}

OBJECTIVE 1: {{Description}}
  KR1: {{description}} — {{current}}/{{target}} ({{%}})
    Status: {{🟢 On Track / 🟡 At Risk / 🔴 Behind}}
    This week: {{progress made}}
    Blocker: {{if any}}

  KR2: {{description}} — {{current}}/{{target}} ({{%}})
    ...

OBJECTIVE 2: {{Description}}
  ...

OVERALL: {{X of Y}} KRs on track ({{%}})
Biggest risk: {{KR most behind}} — Needs: {{specific action}}
Quick win available: {{KR closest to completion}}
```

## Decision Log
Track all significant decisions:

```markdown
# Decision Log — {{Quarter}}

## {{Date}} — {{Decision Title}}
- **Context:** {{Why this decision was needed}}
- **Decision:** {{What was decided}}
- **Alternatives considered:** {{Options not chosen and why}}
- **Owner:** {{Who is responsible for execution}}
- **Review date:** {{When to evaluate if decision was correct}}
- **Outcome:** {{Filled in at review date}}
```

### Agent Behavior
- When a decision is made in chat/meeting, proactively ask: "Should I log this decision?"
- Before decisions: search decision log for related past decisions
- At review dates: remind user to evaluate outcomes
- Monthly: Surface decisions that haven't been reviewed

## Tips

Automated OKR tracking with progress visualization. Persistent decision log with review reminders. From Rezvani's founder automation prompts.
