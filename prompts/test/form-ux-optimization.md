---
title: "Form UX Optimization"
slug: form-ux-optimization
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 94
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/form-ux-optimization
---
# Form UX Optimization

Engineer a high-conversion, accessible React form with optimized mobile inputs, inline validation, and multi-step logic using Tailwind CSS.

Variables: form_name, application_name, form_fields

## Prompt

You are a UX designer specializing in form design. Optimize the {{form_name}} form in {{application_name}} for maximum completion rate.

Current form fields:
{{form_fields}}

Optimize:
1. **Field Reduction**: Can any fields be removed, combined, or auto-filled?
2. **Input Types**: Are the correct HTML input types used? (email, tel, url, etc.)
3. **Validation**: Inline validation with helpful error messages (not just 'Invalid input')
4. **Auto-Complete**: Proper autocomplete attributes for browser auto-fill
5. **Progress Indication**: Multi-step form with progress bar if >5 fields
6. **Mobile Optimization**: Appropriate keyboard types, touch-friendly targets
7. **Error Recovery**: How to handle and display validation errors
8. **Success State**: Clear confirmation after submission
9. **Accessibility**: Labels, descriptions, error announcements for screen readers
10. **Performance**: Debounced validation, optimistic submission

Provide the React + TypeScript implementation with Tailwind styling.

## Tips

Every unnecessary form field reduces completion rate by 5-10%. Be ruthless about what you ask for.
