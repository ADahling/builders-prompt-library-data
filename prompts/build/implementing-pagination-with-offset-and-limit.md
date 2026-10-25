---
title: "Implementing Pagination with Offset and Limit"
slug: implementing-pagination-with-offset-and-limit
stage: Build
category: "API Design"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-pagination-with-offset-and-limit
---
# Implementing Pagination with Offset and Limit

Design an offset-and-limit API endpoint with total counts, pagination metadata, and example requests and responses for item lists.

Variables: offset, limit, items

## Prompt

Design an API endpoint that supports pagination using offset and limit. For example, create a {GET /items} endpoint that accepts {{offset}} and {{limit}} parameters. Discuss:
- How to calculate total items and return metadata in the response.
- What the response structure should look like, including {{items}} and {paginationInfo}.
- Example requests and responses demonstrating this pagination.

## Tips

This prompt will help you implement a common yet effective pagination pattern.
