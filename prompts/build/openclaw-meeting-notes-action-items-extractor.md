---
title: "OpenClaw: Meeting Notes & Action Items Extractor"
slug: openclaw-meeting-notes-action-items-extractor
stage: Build
category: "OpenClaw"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-meeting-notes-action-items-extractor
---
# OpenClaw: Meeting Notes & Action Items Extractor

Turn meeting transcripts or recording descriptions into summaries, decisions, prioritized action items, and open questions for follow-up.

Variables: type, description, who, date, task, name, question

## Prompt

# Meeting Notes & Action Items Extractor

## Input
Provide:
- Meeting transcript (raw text, Zoom/Teams/Otter.ai export)
- OR audio recording description
- Meeting type: {{type}} (standup / planning / retrospective / 1:1 / all-hands / client)

## Processing Pipeline

### Step 1: Structure Raw Notes
- Identify speakers and attribute statements
- Group discussion by topic/agenda item
- Mark timestamps for key moments

### Step 2: Extract Key Components

#### Decisions Made
Format: "[DECISION] {{description}} — decided by {{who}}, on {{date}}"
- Flag decisions that need broader communication
- Note any dissenting opinions

#### Action Items
Format: "[ACTION] {{task}} — Owner: {{name}}, Due: {{date}}"
| Priority | Criteria |
|----------|----------|
| P0 | Blocks other work, mentioned as urgent |
| P1 | Important, has a deadline |
| P2 | Nice to have, no hard deadline |

#### Open Questions
Format: "[QUESTION] {{question}} — needs answer from {{who}}"
- Track unanswered questions
- Suggest who should answer based on context

#### Parking Lot
Items raised but deferred to future discussion.

### Step 3: Generate Summary
- 3-5 bullet executive summary
- Key decisions (numbered)
- Action items table (owner, task, due date, priority)
- Open questions list
- Next meeting date/agenda suggestions

## Output Formats
- Slack message (concise, emoji-formatted)
- Email summary (professional, structured)
- Jira/Linear tickets (auto-create from action items)
- Notion/Confluence page (detailed record)

## Quality Rules
- Never fabricate statements not in the transcript
- Mark uncertain attributions with [?]
- Flag conflicting statements from the same meeting

## Tips

Extracts decisions, action items, and open questions from meeting transcripts. Outputs structured summaries in multiple formats.
