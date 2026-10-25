---
title: "Implement Responsive Design for Complex Data Tables"
slug: implement-responsive-design-for-complex-data-tables
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-responsive-design-for-complex-data-tables
---
# Implement Responsive Design for Complex Data Tables

Convert complex data tables into mobile-friendly components using card layouts, column prioritization, and CSS media queries for any device.

Variables: table_html_structure, table_data_complexity, critical_columns, target_breakpoints

## Prompt

As a front-end engineer, you need to transform a static, wide data table into a fully responsive component that remains usable and visually appealing across a range of screen sizes, from mobile phones to large desktops. The table contains multiple columns and potentially long text content, making simple horizontal scrolling insufficient for a good user experience. Your task is to provide a comprehensive strategy, including specific CSS and potentially HTML modifications.

Input:
- `{{table_html_structure}}`: The complete HTML structure of the data table (e.g., `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`).
- `{{table_data_complexity}}`: A description of the data (e.g., '5 columns, mostly short text', '10 columns, some long URLs and numbers').
- `{{critical_columns}}`: An array of column headers that are absolutely essential to remain visible at all times, even on the smallest screens.
- `{{target_breakpoints}}`: A list of CSS breakpoints your application targets (e.g., `480px`, `768px`, `1024px`).

Instructions:
1. For smaller screens, propose a method to make the table content accessible without excessive horizontal scrolling. Consider techniques such as:
    a. Using `overflow-x: auto` on a wrapper for basic responsiveness.
    b. Transforming rows into 'card-like' layouts where `<th>` elements become `data-label` attributes for `<td>` elements on small screens.
    c. Prioritizing column visibility, potentially hiding less critical columns with media queries and providing a toggle to show/hide them.
2. Provide the necessary CSS (with media queries) and any suggested HTML attribute additions (e.g., `data-label`).
3. Ensure the solution maintains readability and data integrity.
4. Explain the trade-offs of the chosen approach for different screen sizes.

Output Format:
Present the modified HTML structure (if any) and the complete CSS code block, including media queries. Follow this with a detailed explanation of the chosen strategy, its implementation, and how it addresses responsiveness for the given table complexity.

## Tips

This prompt requires a robust understanding of responsive design techniques beyond simple fluid layouts, specifically for data-heavy components.
