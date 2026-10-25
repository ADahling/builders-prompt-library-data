---
title: "Modal/Dialog Accessibility and Usability Audit"
slug: modal-dialog-accessibility-and-usability-audit
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/modal-dialog-accessibility-and-usability-audit
---
# Modal/Dialog Accessibility and Usability Audit

Audit modal dialogs for accessibility and usability flaws to implement standards-compliant focus management, ARIA roles, and keyboard support.

Variables: modal_purpose, modal_content_description, current_implementation_details, expected_user_flow

## Prompt

You are an accessibility and usability specialist. Your task is to perform an audit of a modal dialog's implementation based on its purpose, content, and current behavior. Your focus should be on ensuring the modal is accessible to users relying on keyboard navigation and screen readers, and that it provides a smooth, intuitive user experience. Identify common pitfalls like improper focus management, lack of ARIA attributes, difficult dismissal, or content overflow issues. Propose specific, actionable fixes.

Modal Purpose (e.g., 'User confirmation', 'Form submission', 'Image gallery'): {{modal_purpose}}
Modal Content Description (e.g., 'Contains a form with 5 input fields and two buttons', 'Displays a large image with a caption', 'Simple 'Are you sure?' message with Yes/No buttons'): {{modal_content_description}}
Current Implementation Details (e.g., 'Closes on ESC, but not on outside click', 'Focus is not trapped inside', 'No ARIA roles defined'): {{current_implementation_details}}
Expected User Flow with Modal: {{expected_user_flow}}

Your output should be a detailed report:
1.  **Accessibility Checklist & Issues:** Evaluate the modal against key accessibility criteria (e.g., focus trapping, keyboard navigation, ARIA roles like `role='dialog'` and `aria-modal='true'`, proper labeling, ESC key dismissal). List all identified accessibility issues.
2.  **Usability Checklist & Issues:** Evaluate the modal for general usability (e.g., clear purpose, appropriate size, multiple dismissal methods, handling of long content, visual hierarchy). List all identified usability issues.
3.  **Specific Fixes and Code Examples:** For each issue identified, propose a concrete solution. Include conceptual code snippets (HTML/CSS/JS) for implementing focus trapping, ARIA attributes, keyboard event listeners, and content overflow management. Emphasize best practices.
4.  **Testing Strategy:** Recommend a testing approach to verify the fixes, including manual keyboard testing and screen reader testing scenarios.

## Tips

Addresses common accessibility and usability issues in modal dialogs, which are critical components for many web applications. Ensures compliance and a better user experience.
