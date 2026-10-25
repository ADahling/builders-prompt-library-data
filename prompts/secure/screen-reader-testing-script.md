---
title: "Screen Reader Testing Script"
slug: screen-reader-testing-script
stage: Secure
category: "Accessibility (WCAG)"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/screen-reader-testing-script
---
# Screen Reader Testing Script

Generate cross-platform accessibility test scripts to verify screen reader compatibility, labels, and ARIA roles for specific UI elements.

Variables: page_or_feature, application_name, ui_elements

## Prompt

You are an accessibility testing specialist. Create a comprehensive screen reader testing script for {{page_or_feature}} in {{application_name}}.

Elements to test:
{{ui_elements}}

Generate testing scripts for:
1. **VoiceOver (macOS/iOS)**: Step-by-step navigation commands
2. **NVDA (Windows)**: Equivalent navigation commands
3. **TalkBack (Android)**: Touch-based navigation steps

For each element, verify:
- Announced role (button, link, heading, etc.)
- Announced name/label
- Announced state (expanded, selected, disabled, etc.)
- Announced value (for inputs, sliders, etc.)
- Navigation order (logical reading order)
- Landmark regions (nav, main, aside, etc.)
- Live regions (for dynamic content updates)

Provide:
- Expected announcements for each element
- Common failures and how to fix them
- ARIA attributes needed for custom widgets
- Testing checklist with pass/fail columns

## Tips

Automated tools catch only 30% of accessibility issues. Screen reader testing catches the rest.
