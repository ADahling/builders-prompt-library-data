---
title: "OpenClaw: Documentation Linter & Style Guide"
slug: openclaw-documentation-linter-style-guide
stage: Build
category: "OpenClaw"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-documentation-linter-style-guide
---
# OpenClaw: Documentation Linter & Style Guide

Documentation Linter & Style Guide Input Provide documentation text Markdown, README, API docs, guides for review.

## Prompt

# Documentation Linter & Style Guide

## Input
Provide documentation text (Markdown, README, API docs, guides) for review.

## Style Rules

### Clarity
- Use active voice: "The function returns" not "The value is returned by"
- One idea per sentence, max 25 words
- Define acronyms on first use
- Avoid weasel words: "simply", "just", "easily", "obviously"

### Structure
- Every doc needs: title, purpose statement, audience, prerequisites
- Use progressive disclosure: overview → quickstart → detailed reference
- Max heading depth: H4 (avoid H5+)
- Code examples required for every API endpoint or function

### Code Examples
- Must be copy-pasteable (no pseudo-code in quickstarts)
- Show expected output
- Include error handling
- Use realistic values (not "foo", "bar", "test")
- Specify language in fenced code blocks

### Consistency
- Tense: present tense for descriptions, imperative for instructions
- Lists: parallel structure (all start with verbs, or all are nouns)
- Terminology: maintain a glossary, use consistently throughout
- Formatting: bold for UI elements, code for CLI commands and file paths

## Checks
| Check | Pass | Fail |
|-------|------|------|
| Has purpose statement | ✅ | "What does this doc cover?" missing |
| Code blocks have language | ✅ | ``` without language identifier |
| Links are not broken | ✅ | 404 or relative link errors |
| No TODO/FIXME in published docs | ✅ | Placeholder content shipped |
| Images have alt text | ✅ | `![](image.png)` without alt |
| Consistent heading hierarchy | ✅ | Skipped heading levels |

## Output
- Issue count by severity (error / warning / info)
- Specific line-by-line feedback
- Rewrite suggestions for flagged sections
- Readability score (Flesch-Kincaid grade level target: 8-10)

## Tips

Lints documentation for clarity, structure, code examples, and consistency. Outputs line-by-line feedback with rewrite suggestions.
