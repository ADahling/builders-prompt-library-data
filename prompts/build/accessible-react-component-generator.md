---
title: "Accessible React Component Generator"
slug: accessible-react-component-generator
stage: Build
category: "Frontend & Styling"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/accessible-react-component-generator
---
# Accessible React Component Generator

Build a React component targeting WCAG 2.1 AA with strict TypeScript, Tailwind styling, accessibility comments, and screen reader test cases.

## Prompt

Generate a WCAG 2.1 AA compliant React component for [describe component]:

Requirements:
1. TypeScript with strict types for all props (no "any").
2. Semantic HTML — use the correct element, not div-with-onClick.
3. Keyboard navigation: Tab, Enter, Escape, Arrow keys where appropriate.
4. Screen reader support: meaningful ARIA labels, live regions for dynamic content.
5. Focus management: visible focus indicator, logical tab order, focus trapping for modals.
6. Color contrast: all text meets 4.5:1 ratio. Don't convey meaning through color alone.
7. Touch targets: minimum 44x44px on mobile.
8. Motion: respect prefers-reduced-motion media query.
9. States: loading, error, empty, disabled — all accessible.
10. Testing: include accessibility test cases (what to verify with a screen reader).

Use Tailwind CSS for styling. Use shadcn/ui patterns where applicable.

Provide the complete component with inline comments explaining accessibility decisions.

## Tips

Adapted from AI Prompt Library's React accessibility prompts. Most AI-generated components fail basic accessibility. Source: aipromptlibrary.app/blog/react-javascript-prompts
