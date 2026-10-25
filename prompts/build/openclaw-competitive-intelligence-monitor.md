---
title: "OpenClaw: Competitive Intelligence Monitor"
slug: openclaw-competitive-intelligence-monitor
stage: Build
category: "OpenClaw"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-competitive-intelligence-monitor
---
# OpenClaw: Competitive Intelligence Monitor

Set up daily competitor scans and weekly digests covering announcements, hiring, sentiment, market trends, opportunities, and threats.

Variables: Competitor 1: name, website, social handles, Competitor 2: name, website, social handles, Competitor 3: name, website, social handles, Date, COMPETITOR 1, New features, pricing changes, New roles posted — infer strategy, App store rating change, social mentions, Strategic interpretation, COMPETITOR 2, Industry trend affecting all competitors, Regulatory change to watch, Gap in competitor offering we could exploit, Customer complaint pattern about competitor, Competitor strength that's growing, New entrant to watch

## Prompt

# Competitive Intelligence Monitor — OpenClaw Automation

## Schedule
- **Daily (6 AM):** Quick scan for breaking competitor news
- **Weekly (Monday 8 AM):** Comprehensive competitive digest

## Monitoring Sources
- Competitor websites (pricing pages, blog posts, changelog)
- Product Hunt and Hacker News mentions
- Twitter/X mentions and executive posts
- LinkedIn company pages and employee posts
- App store reviews (ratings changes, new reviews)
- Job postings (infer strategy from hiring patterns)
- Patent filings and press releases
- GitHub repos (for open-source competitors)

## Competitors to Track
Configured in USER.md:
- {{Competitor 1: name, website, social handles}}
- {{Competitor 2: name, website, social handles}}
- {{Competitor 3: name, website, social handles}}

## Weekly Digest Format
```
🔍 COMPETITIVE INTEL — Week of {{Date}}

{{COMPETITOR 1}}
  📢 Announcements: {{New features, pricing changes}}
  👥 Hiring: {{New roles posted — infer strategy}}
  📊 Sentiment: {{App store rating change, social mentions}}
  💡 Insight: {{Strategic interpretation}}

{{COMPETITOR 2}}
  ...

MARKET TRENDS
  - {{Industry trend affecting all competitors}}
  - {{Regulatory change to watch}}

OPPORTUNITIES
  - {{Gap in competitor offering we could exploit}}
  - {{Customer complaint pattern about competitor}}

THREATS
  - {{Competitor strength that's growing}}
  - {{New entrant to watch}}
```

## Alerts (Immediate)
- Competitor raises funding
- Competitor acquires a company
- Major pricing change
- Feature that directly competes with our core value prop

## Tips

Monitors competitors across multiple channels. Infers strategy from hiring patterns and product changes. Weekly digest with opportunities and threats. From Rezvani's founder prompts.
