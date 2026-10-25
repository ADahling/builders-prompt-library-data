---
title: "Designing a Search API"
slug: designing-a-search-api
stage: Build
category: "API Design"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-search-api
---
# Designing a Search API

Plan a search API with query parameters, paginated responses, filtering and performance considerations, and request and response examples.

Variables: items, query, category, sort

## Prompt

Outline a search API that enables users to search for {{items}} based on various criteria. Include:
- Endpoint structure for {GET /search} with query parameters like {{query}}, {{category}}, and {{sort}}.
- Response format that includes relevant fields such as {{items}}, {totalCount}, and {paginationInfo}.
- Implementation considerations like full-text search, filtering options, and performance optimizations.
- Example requests and responses demonstrating typical use cases.

## Tips

This prompt will help you build a powerful search functionality within your API.
