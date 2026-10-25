---
title: "CARE Framework: Accessible UI Prompt Template"
slug: care-framework-accessible-ui-prompt-template
stage: Secure
category: "Accessibility (WCAG)"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/care-framework-accessible-ui-prompt-template
---
# CARE Framework: Accessible UI Prompt Template

Build a UI component using CARE, with accessibility rules for semantics, keyboard use, contrast, focus, and motion, plus good and bad examples.

## Prompt

Use the CARE framework for every UI component you generate:

C — CONTEXT: Describe the component, its purpose, where it appears, and who uses it (include users with disabilities).

A — ASK: State exactly what you need built. Be specific about interactive behavior, states, and data displayed.

R — RULES: Apply these accessibility rules to every component:
- Use semantic HTML elements (<button>, <nav>, <main>, <article>) — not <div> with onClick
- All interactive elements must be keyboard accessible (Tab, Enter, Escape, Arrow keys)
- All images must have meaningful alt text (or alt="" for decorative)
- Color contrast must meet WCAG AA (4.5:1 for text, 3:1 for large text)
- Focus must be visible (never outline: none without a replacement)
- All form inputs must have associated <label> elements
- ARIA attributes only when semantic HTML is insufficient
- Touch targets minimum 24x24px (WCAG 2.5.8), prefer 44x44px on mobile
- No content conveyed by color alone
- Motion must respect prefers-reduced-motion

E — EXAMPLES: Provide a good and bad example of the component for reference.

Apply this framework now to: [describe your component].

## Tips

The CARE framework from UXMagic.ai. Produces significantly more accessible output than generic prompts. Source: uxmagic.ai/blog/prompting-ai-wcag-22-accessible-ui
