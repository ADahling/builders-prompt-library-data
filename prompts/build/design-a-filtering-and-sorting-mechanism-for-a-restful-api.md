---
title: "Design a Filtering and Sorting Mechanism for a RESTful API"
slug: design-a-filtering-and-sorting-mechanism-for-a-restful-api
stage: Build
category: "API Design"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-filtering-and-sorting-mechanism-for-a-restful-api
---
# Design a Filtering and Sorting Mechanism for a RESTful API

Get REST API query syntax for filtering and sorting collection endpoints, with explanations and at least three examples for each.

## Prompt

I want to allow clients of my RESTful API to filter and sort the results of a collection endpoint (e.g., '/products').

Your task is to design a flexible and intuitive filtering and sorting mechanism.

**Instructions:**
1.  **Filtering:** Design a query parameter syntax for filtering. It should support:
    *   Equality checks (e.g., '/products?category=electronics')
    *   Range queries (e.g., '/products?price[gte]=100&price[lte]=500')
    *   Filtering on multiple fields (e.g., '/products?category=electronics&brand=samsung')
2.  **Sorting:** Design a query parameter syntax for sorting. It should support:
    *   Sorting by a single field (e.g., '/products?sort=price')
    *   Ascending and descending order (e.g., '/products?sort=-price')
    *   Sorting by multiple fields (e.g., '/products?sort=category,-price')

**Output Format:**
Provide the output as a Markdown document. For both filtering and sorting, explain the designed syntax and provide at least three examples for each.
