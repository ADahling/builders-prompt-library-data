---
title: "OpenClaw: Personal CRM with Contact Discovery"
slug: openclaw-personal-crm-with-contact-discovery
stage: Build
category: "OpenClaw"
grade: B
score: 77
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-personal-crm-with-contact-discovery
---
# OpenClaw: Personal CRM with Contact Discovery

Set up a personal CRM with Gmail and Calendar contact discovery, duplicate merging, relationship scores, and daily attendee briefings.

Variables: LinkedIn/web research summary

## Prompt

# Personal CRM with Automatic Contact Discovery — OpenClaw Project

## Schedule
- **6:00 AM daily:** Scan Gmail + Google Calendar for contacts
- **7:00 AM daily:** Generate briefing on today's external attendees

## Architecture
### Data Model (SQLite)
```sql
contacts (
  id, name, email, company, role, source,
  first_seen, last_contact, relationship_score,
  notes, tags, linkedin_url
)
interactions (
  id, contact_id, type, date, summary, sentiment
)
follow_ups (
  id, contact_id, due_date, action, status
)
```

### Contact Discovery Pipeline
1. Scan Gmail (using gog CLI) for new email addresses
2. Scan Google Calendar for meeting attendees
3. Auto-filter noise: newsletters, no-reply, automated emails
4. Build/update contact profiles with:
   - Name and email
   - Company (from email domain)
   - Role (if discoverable from email signature)
   - Interaction history (emails exchanged, meetings attended)
5. Duplicate detection: merge contacts with same person, different emails
6. Relationship health score: based on recency, frequency, and reciprocity

### Morning Briefing
```
👤 TODAY'S CONTACTS

9:00 AM — Product Review with Acme Corp
  - Sarah Chen (VP Product) — Last contact: 3 days ago
    Recent: Discussed Q2 roadmap alignment
    Note: She mentioned budget concerns in last email
  - Mike Torres (Engineering Lead) — New contact
    Background: {{LinkedIn/web research summary}}

2:00 PM — Investor Check-in
  - James Park (Partner, Sequoia) — Last contact: 14 days ago
    Follow-up due: Send updated metrics deck
```

### Natural Language Queries
- "Who haven't I talked to in over 30 days?"
- "Show me all contacts from Stripe"
- "Who needs follow-up this week?"
- "What's my history with sarah@acme.com?"

## Tips

Scans Gmail and Calendar daily to build a CRM. Provides meeting briefings with context on each attendee. From DataCamp and mberman84's gist.
