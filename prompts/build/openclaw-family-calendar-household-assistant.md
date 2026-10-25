---
title: "OpenClaw: Family Calendar & Household Assistant"
slug: openclaw-family-calendar-household-assistant
stage: Build
category: "OpenClaw"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-family-calendar-household-assistant
---
# OpenClaw: Family Calendar & Household Assistant

Set up family briefings, calendar conflict checks, approval-ready message replies, and appointment reminders for household scheduling.

Variables: Day, Date, number

## Prompt

# Family Calendar & Household Assistant — OpenClaw Project

## Schedule
- **8:00 AM:** Morning briefing with all family calendars merged
- **Every 15 minutes:** Ambient iMessage monitoring for scheduling mentions

## Morning Briefing
```
🏠 FAMILY BRIEFING — {{Day, Date}}

TODAY:
  🧑 You: 9am Product standup | 2pm Client call | 5pm Dentist
  👩 Partner: 10am Team meeting | 3pm School pickup
  🧒 Kids: School 8-3 | Soccer practice 4pm

⚠️ CONFLICTS:
  - 3pm: You have client call + partner has school pickup
    Suggestion: Can you take the call remote from school parking lot?

🌤️ WEATHER: 72°F, partly cloudy. Rain expected after 6pm.

NEXT 3 DAYS:
  - Tomorrow: No conflicts
  - Thursday: ⚠️ Parent-teacher conference 4pm (both calendars)
  - Friday: Date night reminder (babysitter confirmed?)

🛒 HOUSEHOLD:
  - Grocery list has 8 items (last updated 2 days ago)
  - Package arriving today (Amazon, order #{{number}})
```

## Ambient Monitoring
- Scan iMessage every 15 minutes for scheduling keywords
- When someone texts "Can we do Tuesday at 3?":
  - Check all family calendars
  - Draft response with availability
  - Queue for approval before sending

## Auto-Calendar
- Detect appointment confirmations in messages
- Auto-create calendar events with details
- Add travel time buffers based on location
- Send reminder 1 hour before events with travel info

## Tips

Pulls all family calendars into a single briefing. Ambient iMessage monitoring for scheduling. 3-day conflict lookahead with weather. From DataCamp's 9 OpenClaw Projects.
