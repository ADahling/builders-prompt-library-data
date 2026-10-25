---
title: "Accessibility Audit Checklist Generator"
slug: accessibility-audit-checklist-generator
stage: Design
category: "UX/UI Design"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/accessibility-audit-checklist-generator
---
# Accessibility Audit Checklist Generator

Generate a WCAG 2.2 checklist with testing steps and code examples to ensure specific UI components meet global digital accessibility standards.

Variables: page_or_component_name, application_name, ui_elements_description

## Prompt

You are a WCAG 2.2 accessibility expert. Generate a comprehensive accessibility audit checklist for {{page_or_component_name}} in {{application_name}}.

The component/page includes:
- {{ui_elements_description}}

Generate a checklist organized by WCAG principle:

**Perceivable:**
- Color contrast ratios (AA and AAA)
- Text alternatives for images
- Captions and audio descriptions
- Content adaptability

**Operable:**
- Keyboard navigation (tab order, focus management)
- Touch targets (minimum 44x44px)
- Motion and animation (prefers-reduced-motion)
- Time limits and auto-play

**Understandable:**
- Error identification and suggestions
- Labels and instructions
- Consistent navigation
- Language attributes

**Robust:**
- Valid HTML semantics
- ARIA roles and properties
- Screen reader compatibility
- Browser/AT compatibility

For each item, provide: the WCAG criterion number, how to test it, and a code example of the correct implementation.

## Tips

Run this for every new page or component before shipping. Catches 90% of accessibility issues.
