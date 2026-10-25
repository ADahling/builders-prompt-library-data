---
title: "Pagination Patterns for a RESTful API"
slug: pagination-patterns-for-a-restful-api
stage: Build
category: "API Design"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/pagination-patterns-for-a-restful-api
---
# Pagination Patterns for a RESTful API

Get a REST API pagination strategy comparing offset and cursor methods, with data-change edge cases and example requests and responses.

Variables: items, page, limit, cursor

## Prompt

Develop a pagination strategy for a RESTful API endpoint that returns a list of {{items}}. Discuss the following:
- How to implement offset-based pagination (using {{page}} and {{limit}} parameters) and keyset pagination (using {{cursor}}).
- The pros and cons of each method.
- How to handle edge cases, such as changes in data during pagination (e.g., items being added or removed).
- Provide example requests and expected responses for both pagination methods.

## Tips

This prompt will guide you in creating an efficient and user-friendly way to explore large sets of data.
