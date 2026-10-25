---
title: "OpenClaw: Daily Reddit Digest"
slug: openclaw-daily-reddit-digest
stage: Build
category: "OpenClaw"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-daily-reddit-digest
---
# OpenClaw: Daily Reddit Digest

Set up a daily Telegram digest of relevant subreddit posts, key takeaways, and notable comments, with curation adjusted by feedback.

Variables: subreddit1, subreddit2, subreddit3, Date, Title, upvotes, comments, 1-2 sentences, quote, username

## Prompt

# Daily Reddit Digest — OpenClaw Automation

## Schedule
Cron: Every day at 8:00 AM

## Configuration
Subreddits to monitor (customize in USER.md):
- r/{{subreddit1}}
- r/{{subreddit2}}
- r/{{subreddit3}}

## Pipeline
1. Use reddit-readonly skill to pull hot/new/top posts from each subreddit
2. Score posts by: upvotes, comment quality, relevance to user's interests
3. Filter out: memes (unless specifically subscribed), reposts, low-effort content
4. Extract key discussions: top 3 comments per post, expert opinions
5. Cross-reference with user's knowledge base for related saved content

## Output
Deliver filtered digest to Telegram topic:

```
📱 REDDIT DIGEST — {{Date}}

r/{{subreddit1}}
1. **{{Title}}** ({{upvotes}}↑, {{comments}} comments)
   Key takeaway: {{1-2 sentences}}
   Best comment: "{{quote}}" — u/{{username}}

2. **{{Title}}** ({{upvotes}}↑)
   Key takeaway: {{1-2 sentences}}

---
r/{{subreddit2}}
...
```

## Feedback Loop
- After delivery, ask: "How was today's list? Anything I should add/remove?"
- Track preferences in memory: topics that get engagement vs. ignored
- Sharpen curation over weeks based on feedback
- Maintain a "learned preferences" section in MEMORY.md

## Tips

Cron-triggered Reddit digest with a feedback loop that improves curation over time. From DataCamp's 9 OpenClaw Projects.
