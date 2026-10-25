---
title: "OpenClaw: Morning News Briefing"
slug: openclaw-morning-news-briefing
stage: Build
category: "OpenClaw"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-morning-news-briefing
---
# OpenClaw: Morning News Briefing

Set up a daily news briefing with ranked headlines, source links, calendar context, and a focus suggestion delivered to your chat channel.

Variables: Date, Headline, 1-sentence summary, url, Stock, price, change, time, event, attendee context from CRM, suggestion

## Prompt

# Morning News Briefing — OpenClaw Automation

## Schedule
Cron: Every day at 7:00 AM (user's timezone from USER.md)

## Pipeline
1. Pull headlines from configured sources:
   - Tech: Hacker News top 30, The Verge, Ars Technica
   - AI: Papers With Code trending, AI news aggregators
   - Finance: Bloomberg, Reuters, user's watchlist stocks
2. Scan Twitter/X for trending topics in user's interest areas
3. Check Reddit front pages of subscribed subreddits
4. Filter aggressively — remove duplicates, clickbait, low-signal stories
5. Rank by impact: How much does this affect the user's work or interests?

## Output Format
Save to: ~/clawd/daily/YYYY-MM-DD-news-briefing.md

```markdown
# Daily Briefing — {{Date}}

## 🔴 Must-Read (2-3 items)
- **{{Headline}}** — {{1-sentence summary}} — [Source]({{url}})

## 🟡 Worth Knowing (5-7 items)
- **{{Headline}}** — {{1-sentence summary}} — [Source]({{url}})

## 📈 Markets (if configured)
- {{Stock}}: ${{price}} ({{change}})

## 📅 Today's Calendar
- {{time}} — {{event}} ({{attendee context from CRM}})

## 🎯 Focus Suggestion
Based on your calendar and task list, I recommend focusing on: {{suggestion}}
```

Also deliver summary to configured messaging channel (Telegram/Slack/Discord).

## Tips

Cron-scheduled daily news automation. Pulls from multiple sources, filters aggressively, ranks by personal impact. From Analytics Vidhya and DataCamp.
