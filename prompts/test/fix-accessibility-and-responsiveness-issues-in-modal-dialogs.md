---
title: "Fix Accessibility and Responsiveness Issues in Modal Dialogs"
slug: fix-accessibility-and-responsiveness-issues-in-modal-dialogs
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 98
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-accessibility-and-responsiveness-issues-in-modal-dialogs
---
# Fix Accessibility and Responsiveness Issues in Modal Dialogs

Audit and remediate modal dialogs for WCAG compliance, keyboard focus trapping, and ARIA standards while ensuring mobile responsiveness.

Variables: modal_html_structure, modal_js_logic, target_accessibility_standard

## Prompt

You are an advanced accessibility and front-end development expert. Review the provided HTML structure and JavaScript logic for a modal dialog. Identify and propose detailed fixes for common UX and accessibility issues, including but not limited to: focus trapping, keyboard navigation (Tab, Shift+Tab, Escape), screen reader compatibility (ARIA attributes), proper modal context, and responsiveness across different screen sizes. Ensure that the modal is fully accessible and usable for all users, including those relying on assistive technologies, and degrades gracefully on smaller viewports. Provide specific code modifications for both HTML and JavaScript.

**Modal HTML Structure:**
```html
{{modal_html_structure}}
```

**Modal JavaScript Logic:**
```javascript
{{modal_js_logic}}
```

**Target Accessibility Standard:** `{{target_accessibility_standard}}` (e.g., 'WCAG 2.1 AA', 'ARIA Authoring Practices Guide 1.2')

**Output Format:** Provide a comprehensive report with the following sections:
1.  **Identified Issues:** A bulleted list of all detected UX and accessibility problems.
2.  **Proposed HTML Modifications:** Specific changes to the HTML structure, including ARIA roles, attributes, and semantic elements.
3.  **Proposed JavaScript Modifications:** Detailed changes to the JavaScript logic for focus management, keyboard event handling, and state control.
4.  **Responsiveness Strategy:** Recommendations for making the modal adapt to smaller screens (e.g., full-screen on mobile, fluid sizing).
5.  **Testing Checklist:** A list of key accessibility and responsiveness tests to perform after implementation.

## Tips

This prompt tackles complex accessibility challenges often found in modal dialogs. It requires deep knowledge of ARIA, keyboard interactions, and responsive design principles, making it suitable for advanced developers.
