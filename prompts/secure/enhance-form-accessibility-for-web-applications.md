---
title: "Enhance Form Accessibility for Web Applications"
slug: enhance-form-accessibility-for-web-applications
stage: Secure
category: "Accessibility (WCAG)"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/enhance-form-accessibility-for-web-applications
---
# Enhance Form Accessibility for Web Applications

Audit and refactor web forms to meet WCAG 2.1 AA standards using semantic HTML, ARIA attributes, and keyboard-accessible navigation.

Variables: project_name, tech_stack

## Prompt

You are tasked with ensuring that the web form used in the {{project_name}} project is fully accessible to all users, including those with disabilities. The form is built using {{tech_stack}}. Your goal is to comply with WCAG 2.1 Level AA standards. 

1. Review the existing form structure and identify potential accessibility issues. Pay attention to elements such as input labeling, error messaging, keyboard navigation, and ARIA attributes.

2. Implement semantic HTML elements where applicable and ensure all form fields have associated labels. Use 'aria-label' or 'aria-labelledby' attributes only when necessary and provide clear, descriptive text.

3. Ensure that all form elements are operable via keyboard, including tabbing through fields and activating form controls.

4. Provide clear, concise error messages and ensure they are presented in a way that is accessible to screen readers. Use role='alert' where appropriate to announce errors dynamically.

5. Test the form using a screen reader and make necessary adjustments to ensure a seamless experience.

Output Format:
- Provide a list of identified accessibility issues with brief descriptions.
- Offer a step-by-step guide on how you plan to address each issue.
- Include code snippets where necessary to illustrate your solutions.

Ensure that you provide a detailed explanation for each change and its impact on accessibility.

## Tips

This prompt is ideal when a developer needs to audit and improve the accessibility of a form within a web application. It guides the user through identifying issues, implementing improvements, and testing, ensuring compliance with accessibility standards.
