---
title: "Implement Advanced Filtering and Sorting for a REST API"
slug: implement-advanced-filtering-and-sorting-for-a-rest-api
stage: Build
category: "API Design"
grade: A+
score: 98
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-advanced-filtering-and-sorting-for-a-rest-api
---
# Implement Advanced Filtering and Sorting for a REST API

Design and implement a robust query parameter syntax for multi-field filtering, complex operators, and multi-level sorting in a REST API.

Variables: platform_name, language

## Prompt

You are a lead API developer. Our e-commerce platform, {{platform_name}}, needs a more powerful and flexible way for clients to filter and sort product listings. The current API only supports basic filtering by category. We need to implement a more advanced system.

**Requirements:**

1.  **Filtering:**
    *   Allow filtering by multiple attributes at once (e.g., '/products?brand=Nike&color=blue&price_lt=100').
    *   Support a range of operators: equality ('eq'), not equal ('neq'), greater than ('gt'), less than ('lt'), greater than or equal to ('gte'), less than or equal to ('lte').
    *   Support filtering on nested object properties.
2.  **Sorting:**
    *   Allow sorting by any top-level attribute of the product resource.
    *   Support ascending ('asc') and descending ('desc') order (e.g., '/products?sort=price_asc').
    *   Allow sorting by multiple fields (e.g., '/products?sort=brand_asc,price_desc').
3.  **Implementation:**
    *   Propose a clean and consistent query parameter syntax for filtering and sorting.
    *   Provide a pseudo-code or actual code example (in {{language}}) showing how to parse these query parameters on the backend and dynamically construct a database query (e.g., using an ORM like Prisma or Sequelize).

**Output Format:**
Write a technical specification in Markdown. Clearly define the query parameter syntax. Provide the backend implementation example in a well-commented code block.
