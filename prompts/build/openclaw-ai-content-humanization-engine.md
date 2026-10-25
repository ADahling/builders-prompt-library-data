---
title: "OpenClaw: AI Content Humanization Engine"
slug: openclaw-ai-content-humanization-engine
stage: Build
category: "OpenClaw"
grade: B
score: 70
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-ai-content-humanization-engine
---
# OpenClaw: AI Content Humanization Engine

Review draft content for stock AI phrasing and repetitive structure, then rewrite it with concrete language while preserving voice and intent.

## Prompt

# AI Content Humanization Engine — Detect & Rewrite AI Patterns

Input: Paste draft text (social posts, blog paragraphs, emails, video scripts).

## Step 1 — Detection

Scan for common AI tells based on Wikipedia's "Signs of AI writing" page:

### Phrase-Level Tells
- Overuse of: "delve", "landscape", "leverage", "it's important to note", "in conclusion"
- Tone inflation: "game-changing", "revolutionary", "transformative" when unwarranted
- Generic phrasing that could apply to any topic
- Performed authenticity: "Great question!", "I'd be happy to help!"
- Stock phrases: "holding down the fort", "at the end of the day", "deep dive"

### Structural Patterns
- Excessive em dashes and semicolons
- Rule of three everywhere
- Identical paragraph lengths and rhythms
- Every sentence starting the same way
- Excessive hedging: "It's worth noting that perhaps..."
- Lists that are too clean, too parallel, no personality
- Repetitive sentence structures

## Step 2 — Rewrite Rules
- Replace vague qualifiers with specific, concrete language
- Vary sentence length (mix short punchy with longer ones)
- Use contractions, fragments, informal word choices where natural
- Remove filler while keeping core message
- Add human cadence — not errors, but natural rhythm
- Preserve the author's voice and intent

## Step 3 — Channel Tuning (optional)
- **Twitter/X:** Punchy, <280 chars, direct, no filler
- **LinkedIn:** Professional but conversational, authoritative not stiff
- **Blog:** Longer form, personal anecdotes and opinions welcome
- **Email:** Brief, clear, action-oriented, warm but efficient
- **Video Script:** Conversational, natural pauses, spoken rhythm

## Step 4 — Output
Return revised text. Optionally highlight what changed and why.

## Auto-Apply Mode
Run automatically on any longer piece of user-facing prose.
Add regression tests to catch patterns that keep coming back.

## Tips

Comprehensive AI content humanization engine combining detection, rewriting, channel tuning, and auto-apply. Merged from two OpenClaw humanizer prompts. Based on mberman84's gist.
