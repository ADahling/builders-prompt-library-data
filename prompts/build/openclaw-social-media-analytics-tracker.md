---
title: "OpenClaw: Social Media Analytics Tracker"
slug: openclaw-social-media-analytics-tracker
stage: Build
category: "OpenClaw"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-social-media-analytics-tracker
---
# OpenClaw: Social Media Analytics Tracker

Set up daily social media tracking across five platforms, with SQLite metrics, performance snapshots, and trends for morning briefings.

Variables: Date, count, +/-, avg, title, views, %, new subs / views, metric, text, engagements

## Prompt

# Social Media Analytics Tracker — OpenClaw Automation

## Schedule
Cron: Daily at 11:00 PM (after day's activity settles)

## Platforms Tracked
- YouTube: Channel analytics, per-video metrics
- Instagram: Post performance, story views, follower growth
- X/Twitter: Engagement rates, follower changes, viral tweets
- TikTok: View counts, completion rates, follower growth
- LinkedIn: Post impressions, profile views, connection requests

## Daily Snapshot (SQLite)
```sql
daily_metrics (
  date, platform, followers, following,
  posts_count, total_views, total_engagement,
  top_post_url, top_post_metric
)
per_post_metrics (
  date, platform, post_url, post_date,
  views, likes, comments, shares, saves,
  engagement_rate, completion_rate
)
```

## Analysis Output
```
📊 SOCIAL SNAPSHOT — {{Date}}

YOUTUBE
  Subscribers: {{count}} ({{+/-}} today)
  Views today: {{count}} (30-day avg: {{avg}})
  Top video: "{{title}}" — {{views}} views, {{%}} CTR
  Subscriber conversion: {{new subs / views}}%

INSTAGRAM
  Followers: {{count}} ({{+/-}})
  Story views avg: {{count}} ({{%}} of followers)
  Best post: {{metric}}

X/TWITTER
  Followers: {{count}} ({{+/-}})
  Impressions: {{count}}
  Top tweet: "{{text}}" — {{engagements}}

TRENDS:
  📈 YouTube subscribers accelerating (+12% vs last week)
  📉 Instagram reach declining (-8% over 2 weeks)
  🔄 Twitter engagement flat
```

## Feeds Into
- Daily briefing (morning summary)
- Business advisory council (growth strategist persona)
- Content pipeline (what topics perform best?)

## Tips

Daily social media analytics snapshots stored in SQLite. Tracks per-post and channel-level metrics across platforms. From mberman84's gist.
