---
title: "OpenClaw: Health & Symptom Tracker"
slug: openclaw-health-symptom-tracker
stage: Build
category: "OpenClaw"
grade: C
score: 61
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-health-symptom-tracker
---
# OpenClaw: Health & Symptom Tracker

Health & Symptom Tracker — OpenClaw Automation Concept Telegram-based food, drink, symptom, and wellness tracking.

Variables: date

## Prompt

# Health & Symptom Tracker — OpenClaw Automation

## Concept
Telegram-based food, drink, symptom, and wellness tracking. Lowest-effort OpenClaw project — no skills needed, just prompt + cron.

## Input Format
Message the agent naturally:
- "Ate sushi for lunch, feeling a bit bloated"
- "Coffee at 3pm"
- "Headache started around 2pm, maybe 3/5"
- "Slept 7 hours, woke up groggy"
- "30 min walk, felt great after"

## Processing
1. Parse natural language input into structured entry
2. Timestamp and categorize: food / drink / symptom / exercise / sleep / note
3. Symptom severity: 1-5 scale (extracted from context or ask)
4. Save to: ~/clawd/memory/health-log.md (organized by date)

## Reminders
Cron-scheduled gentle nudges:
- 8:00 AM: "Good morning! What did you have for breakfast?"
- 1:00 PM: "Lunch check-in — what are you eating?"
- 7:00 PM: "Evening log — dinner and how you're feeling?"

## Weekly Analysis
Every Sunday, generate correlation analysis:

```
📊 WEEKLY HEALTH SUMMARY — Week of {{date}}

Patterns Detected:
- Headaches correlated with skipping lunch (3/4 occurrences)
- Sleep quality better on exercise days (+1.2 avg rating)
- Bloating episodes follow dairy consumption (2/3 cases)

Averages:
- Sleep: 6.8 hrs (↓0.3 from last week)
- Exercise: 3 sessions (target: 4)
- Water: ~5 glasses/day (target: 8)
- Mood: 3.8/5 average

Suggestions:
- Consider tracking water intake more consistently
- The dairy-bloating pattern is worth monitoring another week
```

## Privacy
- All data stored locally in Markdown files
- Never synced to cloud
- Never shared with any third party
- User can delete any entry at any time

## Tips

Lowest-effort OpenClaw project — just prompt + cron. No skills needed. Telegram-based tracking with weekly correlation analysis. From DataCamp and Analytics Vidhya.
