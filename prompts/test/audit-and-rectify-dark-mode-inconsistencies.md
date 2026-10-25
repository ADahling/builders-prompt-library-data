---
title: "Audit and Rectify Dark Mode Inconsistencies"
slug: audit-and-rectify-dark-mode-inconsistencies
stage: Test
category: "UX/UI Fixes"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/audit-and-rectify-dark-mode-inconsistencies
---
# Audit and Rectify Dark Mode Inconsistencies

Audit web components for dark mode inconsistencies, contrast, and readability issues, with specific CSS or design token fixes for each problem.

Variables: application_name, component_names, current_dark_mode_styles

## Prompt

Conduct a comprehensive audit of the dark mode implementation for the provided web application components. Identify specific instances where the dark mode styling is inconsistent with the overall design system, lacks sufficient contrast, or presents readability issues. This includes examining text colors, background colors, border colors, icon colors, shadow effects, and interactive element states (hover, active, focus). Your goal is to pinpoint exact CSS/SCSS or theme variable discrepancies and propose precise adjustments to achieve a cohesive, accessible, and aesthetically pleasing dark mode experience. Pay close attention to subtle details like disabled button states, placeholder text, and tertiary UI elements that often get overlooked. Provide actionable code-level suggestions where possible, or clear instructions for updating design tokens.

**Application Name:** {{application_name}}
**Component(s) for Audit:** {{component_names}} (e.g., navigation bar, card components, form inputs, modal dialogs)
**Current Dark Mode CSS/Theme Variables (if available):**
```css
{{current_dark_mode_styles}}
```

**Output Format:** List each identified inconsistency, describe the current problematic styling, explain why it's inconsistent or problematic, and provide a concrete proposed fix. Structure your response with headings for each component and bullet points for specific issues.

## Tips

This advanced prompt helps developers systematically debug and refine dark mode implementations, ensuring consistency and accessibility across complex applications.
