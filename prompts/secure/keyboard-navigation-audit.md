---
title: "Keyboard Navigation Audit"
slug: keyboard-navigation-audit
stage: Secure
category: "Accessibility (WCAG)"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/keyboard-navigation-audit
---
# Keyboard Navigation Audit

Identify keyboard accessibility flaws and WCAG violations in UI components to ensure logical navigation and full ARIA compliance.

Variables: page_or_component, application_name, ui_elements_description

## Prompt

You are a keyboard accessibility expert. Audit the keyboard navigation for {{page_or_component}} in {{application_name}}.

UI elements:
{{ui_elements_description}}

Test and document:
1. **Tab Order**: Is the tab order logical and matches visual order?
2. **Focus Visibility**: Is the focus indicator visible on every interactive element?
3. **Focus Trapping**: Are modals and dropdowns properly trapping focus?
4. **Skip Links**: Is there a 'Skip to main content' link?
5. **Keyboard Shortcuts**: Are all actions accessible via keyboard?
6. **Custom Widgets**: Do custom components (tabs, accordions, menus) follow WAI-ARIA patterns?
7. **Form Navigation**: Can all form fields be reached and submitted via keyboard?
8. **Error Recovery**: Can keyboard users navigate to and understand error messages?

For each issue:
- The element affected
- The keyboard interaction that fails
- The expected behavior
- The fix (HTML/ARIA/JS code)
- The WCAG criterion violated

## Tips

15% of users rely on keyboard navigation. This includes power users, not just users with disabilities.
