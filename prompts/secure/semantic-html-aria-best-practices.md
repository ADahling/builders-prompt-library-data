---
title: "Semantic HTML & ARIA Best Practices"
slug: semantic-html-aria-best-practices
stage: Secure
category: "Accessibility (WCAG)"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/semantic-html-aria-best-practices
---
# Semantic HTML & ARIA Best Practices

Fix semantic HTML and ARIA issues in your components with before-and-after code and descriptions of screen reader announcements.

## Prompt

Review my components and fix all semantic HTML and ARIA issues:

1. REPLACE DIV SOUP: Find every <div> or <span> used as an interactive element and replace with the correct semantic element:
   - Clickable? Use <button>
   - Navigates? Use <a href>
   - List of items? Use <ul>/<ol> + <li>
   - Page section? Use <section>, <article>, <aside>, <nav>, <main>, <header>, <footer>
   - Heading? Use <h1>-<h6> in proper hierarchy (only one <h1> per page)

2. FIX ARIA MISUSE: Remove ARIA attributes that duplicate native HTML semantics:
   - <button role="button"> → just <button>
   - <a role="link"> → just <a>
   - <input aria-required="true"> → <input required>

3. ADD MISSING ARIA: Add ARIA only where semantic HTML is insufficient:
   - Custom dropdown: role="listbox", role="option", aria-expanded
   - Tabs: role="tablist", role="tab", role="tabpanel", aria-selected
   - Modal: role="dialog", aria-modal="true", aria-labelledby
   - Live regions: aria-live="polite" for dynamic content updates
   - Loading states: aria-busy="true"

4. SCREEN READER TESTING: For each component, describe what a screen reader would announce. Flag anything confusing.

Provide before/after code for every fix.

## Tips

The #1 accessibility mistake is using ARIA when semantic HTML would work. 'No ARIA is better than bad ARIA.' Source: uxmagic.ai
