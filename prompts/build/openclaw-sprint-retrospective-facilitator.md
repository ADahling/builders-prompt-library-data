---
title: "OpenClaw: Sprint Retrospective Facilitator"
slug: openclaw-sprint-retrospective-facilitator
stage: Build
category: "OpenClaw"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-sprint-retrospective-facilitator
---
# OpenClaw: Sprint Retrospective Facilitator

Plan a sprint retrospective with rotating discussion formats, a timed facilitation guide, and action items with owners and due dates.

Variables: sprint, goal, yes/no/partial, size, duration, action, name, date, how to measure, previous_action, notes

## Prompt

# Sprint Retrospective Facilitator

## Input
- Sprint number/name: {{sprint}}
- Sprint goal: {{goal}}
- Goal achieved? {{yes/no/partial}}
- Team size: {{size}}
- Sprint duration: {{duration}}

## Retrospective Formats (rotate for freshness)

### Format 1: Start / Stop / Continue
| Category | Prompt |
|----------|--------|
| 🟢 Start | What should we begin doing next sprint? |
| 🔴 Stop | What's not working and should be dropped? |
| 🔵 Continue | What's working well and should keep going? |

### Format 2: 4Ls
| L | Prompt |
|---|--------|
| 💚 Liked | What went well? |
| 📚 Learned | What did we discover? |
| 🤷 Lacked | What was missing? |
| 🔮 Longed for | What do we wish we had? |

### Format 3: Sailboat
| Element | Meaning | Prompt |
|---------|---------|--------|
| 🌬️ Wind | Accelerators | What pushed us forward? |
| ⚓ Anchor | Blockers | What held us back? |
| 🪨 Rocks | Risks | What could sink us ahead? |
| 🏝️ Island | Goals | Where are we trying to get? |

## Facilitation Guide
1. **Set the stage** (5 min): Safety check, remind of prime directive
2. **Gather data** (15 min): Silent brainstorm, sticky notes / virtual board
3. **Group & vote** (10 min): Cluster themes, dot-vote top 3
4. **Generate actions** (15 min): For top 3 themes, define SMART actions
5. **Close** (5 min): Appreciation round, assign action owners

## Action Item Template
| Action | Owner | Due | Success Metric |
|--------|-------|-----|---------------|
| {{action}} | {{name}} | {{date}} | {{how to measure}} |

## Anti-Patterns to Avoid
- ❌ Same format every sprint (rotate!)
- ❌ No action items (retro without actions = venting session)
- ❌ Actions from last retro not reviewed
- ❌ One person dominates discussion
- ❌ Blame instead of systems thinking
- ❌ Skipping retro because "we're too busy"

## Previous Actions Review
Always start by reviewing action items from the last retrospective:
| Action | Status | Notes |
|--------|--------|-------|
| {{previous_action}} | ✅ Done / ⏳ In progress / ❌ Not started | {{notes}} |

## Tips

Facilitates sprint retrospectives with 3 rotating formats (Start/Stop/Continue, 4Ls, Sailboat). Includes facilitation guide and anti-pattern warnings.
