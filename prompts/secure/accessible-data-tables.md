---
title: "Accessible Data Tables"
slug: accessible-data-tables
stage: Secure
category: "Accessibility (WCAG)"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/accessible-data-tables
---
# Accessible Data Tables

Get refactored HTML for a data table with ARIA roles for tables, rows, and cells, plus scope attributes for headers.

## Prompt

Refactor a data table markup to include ARIA attributes for better accessibility. For a table displaying {dataType}, ensure you add roles like 'table', 'row', and 'cell'. Also, include 'scope' attributes for headers. Use the format '<table role='table'> <thead> <tr> <th scope='col'>...</th></tr></thead> <tbody> <tr role='row'> <td role='cell'>...</td></tr></tbody></table>'.

## Tips

This is vital for users who rely on screen readers to navigate tables.
