---
title: "PR Description Generator"
slug: pr-description-generator
stage: Test
category: "Code Review"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/pr-description-generator
---
# PR Description Generator

Generate a clear PR description from this diff: paste your git diff or changed files Format: What One paragraph: what changed and why.

## Prompt

Generate a clear PR description from this diff:

[paste your git diff or changed files]

Format:

## What
One paragraph: what changed and why.

## Why
Link to ticket/issue. Business context for the change.

## How
Technical summary of the approach. Key design decisions.

## Changes
- File-by-file summary of what changed
- New dependencies added (if any)

## Testing
- How was this tested? (unit, integration, manual)
- Steps to test manually:
  1. ...
  2. ...
  3. Expected result: ...

## Screenshots
[placeholder for before/after if UI change]

## Checklist
- [ ] Tests pass
- [ ] No console errors
- [ ] Reviewed own diff before requesting review
- [ ] Documentation updated (if needed)
- [ ] Migration included (if DB changes)

## Tips

Good PR descriptions cut review time in half.
