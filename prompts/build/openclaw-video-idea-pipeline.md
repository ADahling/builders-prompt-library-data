---
title: "OpenClaw: Video Idea Pipeline"
slug: openclaw-video-idea-pipeline
stage: Build
category: "OpenClaw"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-video-idea-pipeline
---
# OpenClaw: Video Idea Pipeline

Video Idea Pipeline — OpenClaw Content Automation Trigger Activated by Slack mentions in designated channel or direct messages containing content ideas.

Variables: Title, First 5 seconds — why should viewer care?, Core argument in 1 sentence, Tutorial / Review / Opinion / Walkthrough, minutes, Section 1, estimated time, Section 2, Section 3, What should viewer do next?, Relevant URL 1, Relevant saved knowledge base entry, similarity score, date, Why this is distinct enough, 1-10, Low/Medium/High

## Prompt

# Video Idea Pipeline — OpenClaw Content Automation

## Trigger
Activated by Slack mentions in designated channel or direct messages containing content ideas.

## Pipeline
1. **Capture:** Read Slack thread context
2. **Research:** Run X/Twitter search for related discussions and trending topics
3. **Enrich:** Query personal knowledge base for related saved content
4. **Dedup:** Semantic similarity search against previous pitches
   - If >40% similar to existing idea → Skip with note
   - If <40% → Proceed to card creation
5. **Create:** Generate structured Asana/Linear card

## Card Format
```
📹 VIDEO IDEA — {{Title}}

Hook: {{First 5 seconds — why should viewer care?}}
Thesis: {{Core argument in 1 sentence}}
Format: {{Tutorial / Review / Opinion / Walkthrough}}
Target length: {{minutes}}

Outline:
1. {{Section 1}} ({{estimated time}})
2. {{Section 2}}
3. {{Section 3}}
4. CTA: {{What should viewer do next?}}

Research Links:
- {{Relevant URL 1}}
- {{Relevant saved knowledge base entry}}

Similar Past Content:
- {{Title}} ({{similarity score}}%) — {{date}}
  Difference: {{Why this is distinct enough}}

Estimated Performance:
- Topic trending score: {{1-10}}
- Audience match: {{1-10}}
- Production effort: {{Low/Medium/High}}
```

## Tracking
- Track pitch status: Pitched → Approved → Scripted → Filmed → Published
- Learn from feedback: Which ideas get approved? Which perform well?
- Weekly idea quality report with win rate

## Tips

Content creation pipeline triggered by Slack. Runs research, deduplicates against past ideas, creates structured project cards. From mberman84's gist.
