---
title: "OpenClaw: Content Pipeline & Campaign Tracker"
slug: openclaw-content-pipeline-campaign-tracker
stage: Build
category: "OpenClaw"
grade: B
score: 77
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-content-pipeline-campaign-tracker
---
# OpenClaw: Content Pipeline & Campaign Tracker

Set up content-stage tracking, deadline reminders, SEO briefs, and campaign reports to monitor publishing work and marketing performance.

Variables: Date, count, title, where idea came from, 1-5, date, person, current, target, date, time, where, platform, metrics after 48h, CAMPAIGN NAME, Start, End, spent, total, %, list of active channels, num, actual, status, Increase/Decrease/Pause, reason

## Prompt

# Content Pipeline & Campaign Tracker — OpenClaw Marketing Automation

## Content Pipeline

### Idea → Published Tracking
```
📝 CONTENT PIPELINE — {{Date}}

IDEAS ({{count}})
  - {{title}} — Source: {{where idea came from}} — Priority: {{1-5}}

RESEARCH ({{count}})
  - {{title}} — Outline due: {{date}} — Assigned: {{person}}

DRAFTING ({{count}})
  - {{title}} — First draft due: {{date}} — Word count: {{current}}/{{target}}

REVIEW ({{count}})
  - {{title}} — Reviewer: {{person}} — Due: {{date}}

SCHEDULED ({{count}})
  - {{title}} — Publish: {{date, time}} — Platform: {{where}}

PUBLISHED THIS WEEK ({{count}})
  - {{title}} — {{platform}} — {{metrics after 48h}}
```

### Automated Actions
- Move ideas from intake channel to pipeline automatically
- Set due dates based on publication calendar
- Remind authors 2 days before draft deadlines
- Generate SEO brief when content moves to "Research"
- Pull engagement metrics 48h after publication

## Campaign Tracker

### Active Campaigns
```
📢 CAMPAIGN STATUS — {{Date}}

{{CAMPAIGN NAME}} ({{Start}} → {{End}})
  Budget: ${{spent}} / ${{total}} ({{%}})
  Channels: {{list of active channels}}
  
  Performance:
  | Channel | Impressions | Clicks | CTR | Conv | CPA |
  |---------|------------|--------|-----|------|-----|
  | Google  | {{num}}    | {{num}}| {{%}}| {{num}}| ${{num}}|
  | Meta    | {{num}}    | {{num}}| {{%}}| {{num}}| ${{num}}|
  
  vs. Targets:
  - CPA: ${{actual}} vs ${{target}} ({{status}})
  - ROAS: {{actual}} vs {{target}} ({{status}})
  
  Recommendation: {{Increase/Decrease/Pause}} — {{reason}}
```

### Alerts
- Budget pacing off (>10% over/under daily target)
- CTR drops below benchmark for 3 consecutive days
- CPA exceeds target by >25%
- Campaign ending in <3 days without renewal plan

## Tips

Content pipeline tracking from idea to published with automated stage management. Campaign tracker with budget pacing and performance alerts. From Rezvani's marketing automation prompts.
