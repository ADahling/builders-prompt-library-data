---
title: "ECC Command: /prune"
slug: ecc-command-prune
stage: Build
category: "AI Agent Development"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ecc-command-prune
---
# ECC Command: /prune

Prune Pending Instincts Remove expired pending instincts that were auto-generated but never reviewed or promoted.

## Prompt

# Prune Pending Instincts

Remove expired pending instincts that were auto-generated but never reviewed or promoted.

## Implementation

Run the instinct CLI using the plugin root path:

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/skills/continuous-learning-v2/scripts/instinct-cli.py" prune
```

Or if `CLAUDE_PLUGIN_ROOT` is not set (manual installation):

```bash
python3 ~/.claude/skills/continuous-learning-v2/scripts/instinct-cli.py prune
```

## Usage

```
/prune                    # Delete instincts older than 30 days
/prune --max-age 60      # Custom age threshold (days)
/prune --dry-run         # Preview without deleting
```

## Tips

Source: Everything Claude Code (ECC) — Command: /prune
