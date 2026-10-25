---
title: "OpenClaw: Accessibility Audit Agent (WCAG 2.2)"
slug: openclaw-accessibility-audit-agent-wcag-2-2
stage: Build
category: "OpenClaw"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-accessibility-audit-agent-wcag-2-2
---
# OpenClaw: Accessibility Audit Agent (WCAG 2.2)

Audit a URL, component, or mockup against accessibility checks for WCAG levels A and AA, plus newer focus and interaction criteria in WCAG 2.2.

## Prompt

# Accessibility Audit Agent — WCAG 2.2

## Input
Provide:
- URL to audit, OR
- HTML/component code to review, OR
- Design mockup description

## Audit Checklist by Level

### Level A (Minimum — must pass)
| Criterion | Check |
|-----------|-------|
| 1.1.1 Non-text Content | All images have meaningful alt text |
| 1.3.1 Info & Relationships | Semantic HTML (headings, lists, tables) |
| 1.4.1 Use of Color | Information not conveyed by color alone |
| 2.1.1 Keyboard | All functionality available via keyboard |
| 2.4.1 Bypass Blocks | Skip navigation link present |
| 2.4.2 Page Titled | Descriptive, unique page titles |
| 3.1.1 Language | Lang attribute on html element |
| 4.1.1 Parsing | Valid HTML, unique IDs |

### Level AA (Standard — should pass)
| Criterion | Check |
|-----------|-------|
| 1.4.3 Contrast | Text: 4.5:1 ratio, large text: 3:1 |
| 1.4.4 Resize Text | Content readable at 200% zoom |
| 1.4.10 Reflow | No horizontal scroll at 320px width |
| 2.4.6 Headings | Descriptive, hierarchical headings |
| 2.4.7 Focus Visible | Clear focus indicator on all interactive elements |
| 3.3.2 Labels | Form inputs have visible labels |

### WCAG 2.2 New Criteria
| Criterion | Check |
|-----------|-------|
| 2.4.11 Focus Not Obscured (AA) | Focus indicator not hidden by sticky headers/modals |
| 2.4.13 Focus Appearance (AAA) | Focus indicator meets size/contrast requirements |
| 2.5.7 Dragging Movements (AA) | Drag operations have non-dragging alternative |
| 2.5.8 Target Size (AA) | Interactive targets ≥ 24×24 CSS pixels |
| 3.3.7 Redundant Entry (A) | Don't ask for same info twice in a flow |

## Output
| Issue | Level | Impact | Location | Fix |
|-------|-------|--------|----------|-----|
| Missing alt text | A | High | img.hero | Add descriptive alt |
| Low contrast | AA | Medium | .subtitle | Change to #333 |

Summary: X issues (Y critical, Z warnings)

## Tips

WCAG 2.2 accessibility audit covering Levels A, AA, and new 2.2 criteria. Outputs prioritized issues with specific fixes.
