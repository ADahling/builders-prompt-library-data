---
title: "OpenClaw: Meeting Action Items Pipeline"
slug: openclaw-meeting-action-items-pipeline
stage: Build
category: "OpenClaw"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-meeting-action-items-pipeline
---
# OpenClaw: Meeting Action Items Pipeline

Meeting Action Items Pipeline — OpenClaw Automation Schedule Poll for new meeting transcripts every 5 minutes during business hours.

Variables: Meeting Title, Date

## Prompt

# Meeting Action Items Pipeline — OpenClaw Automation

## Schedule
Poll for new meeting transcripts every 5 minutes during business hours.

## Pipeline
1. **Fetch transcripts** from Fathom (or Otter.ai, Fireflies, etc.)
2. **Calendar-aware matching:** Link transcript to calendar event
3. **Attendee enrichment:** Match attendees to CRM contact profiles
4. **Action item extraction:**
   - Identify all commitments made in the meeting
   - Classify ownership: Mine vs. Theirs
   - Extract deadlines (explicit or implied)
   - Identify decisions made
   - Flag unresolved questions

## Approval Queue
Send extracted action items to Telegram for approval:

```
📋 ACTION ITEMS — {{Meeting Title}} ({{Date}})

MINE:
1. ✏️ Send updated proposal to Sarah by Friday
2. ✏️ Review competitor pricing analysis
3. ✏️ Schedule follow-up with engineering team

THEIRS:
4. 👤 Sarah: Share Q2 budget numbers
5. 👤 Mike: Send API documentation

DECISIONS:
- Agreed to move launch date to April 15
- Will use Stripe instead of custom payment system

UNRESOLVED:
- Need to decide on pricing tier structure
- Security review timeline TBD
```

User approves/edits items → Approved items become Todoist tasks.

## Follow-Up Tracking
- Check completion 3× daily (10 AM, 2 PM, 5 PM)
- Gentle reminder for items approaching deadline
- Auto-archive completed items after 14 days
- Weekly summary: completion rate, overdue items, blocked items

## Tips

Polls meeting transcripts, extracts action items with ownership, sends approval queue to Telegram, creates tasks. From mberman84's gist.
