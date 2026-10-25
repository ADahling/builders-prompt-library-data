---
title: "Enhancing Table Accessibility for Web Applications"
slug: enhancing-table-accessibility-for-web-applications
stage: Secure
category: "Accessibility (WCAG)"
grade: A
score: 83
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/enhancing-table-accessibility-for-web-applications
---
# Enhancing Table Accessibility for Web Applications

Refactor HTML tables with semantic tags, ARIA attributes, and keyboard navigation to ensure full accessibility for screen reader users.

Variables: web_app_name, data_type, page_name

## Prompt

As a web developer, you are tasked with ensuring that the tables on your website are accessible to all users, including those using screen readers. Your goal is to improve the accessibility of an HTML table used in the {{web_app_name}} project. The table displays {{data_type}} and is located on the {{page_name}} page. Follow these guidelines to make your table accessible: 

1. Use the `<table>`, `<thead>`, `<tbody>`, and `<tfoot>` tags to properly structure your table.
2. Ensure each `<th>` (table header) element has a scope attribute set to either 'col' or 'row' to define the scope of the header.
3. Use the `<caption>` tag to provide a brief description of the table's purpose.
4. Include ARIA attributes where necessary to enhance accessibility, such as `aria-labelledby` or `aria-describedby`.
5. Make sure the table is keyboard navigable by using tabindex where appropriate.

Please provide a code snippet or text explanation on how you would implement these enhancements in the context of the {{web_app_name}} project.

## Tips

Use this prompt when you need to implement or improve the accessibility features of a table within a web application. It guides developers through the necessary steps to ensure tables are accessible to users with disabilities, particularly those using screen readers.
