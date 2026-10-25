---
title: "OpenClaw: Changelog & Release Notes Generator"
slug: openclaw-changelog-release-notes-generator
stage: Build
category: "OpenClaw"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-changelog-release-notes-generator
---
# OpenClaw: Changelog & Release Notes Generator

Turn Git logs, merged PRs, or change lists into a developer changelog, user release notes, and a social post for a product release.

## Prompt

# Changelog & Release Notes Generator

## Input
Provide one of:
- Git log output (git log --oneline v1.2.0..HEAD)
- List of merged PRs with titles
- Bullet-point list of changes

## Classification
Categorize each change:
| Type | Emoji | Description |
|------|-------|-------------|
| Feature | ✨ | New capabilities |
| Fix | 🐛 | Bug fixes |
| Breaking | 💥 | Breaking changes (highlight prominently) |
| Performance | ⚡ | Speed or resource improvements |
| Security | 🔒 | Security patches |
| Deprecation | ⚠️ | Deprecated features |
| Docs | 📝 | Documentation updates |
| Chore | 🔧 | Internal tooling, deps, CI |

## Output Formats

### Developer Changelog (CHANGELOG.md)
```
## [version] — YYYY-MM-DD
### 💥 Breaking Changes
- Description (PR #123)
### ✨ Features
- Description (PR #124)
### 🐛 Bug Fixes
- Description (PR #125)
```

### User-Facing Release Notes
- Plain language, no jargon
- Lead with benefits, not implementation details
- Group by user impact: "What's New", "What's Fixed", "What's Changed"
- Include migration steps for breaking changes

### Social Post (Twitter/LinkedIn)
- 280-char summary with key highlights
- Emoji-rich, action-oriented

## Rules
- Never fabricate changes not in the input
- Flag ambiguous commits for human review
- Sort by impact within each category
- Link PRs/issues when references are available

## Tips

Automates changelog and release notes from git logs or PR lists. Outputs developer changelog, user-facing notes, and social posts.
