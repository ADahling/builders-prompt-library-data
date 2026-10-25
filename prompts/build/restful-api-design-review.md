---
title: "RESTful API Design Review"
slug: restful-api-design-review
stage: Build
category: "API Design"
grade: B
score: 75
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/restful-api-design-review
---
# RESTful API Design Review

Review API endpoints for REST design issues and get corrected versions covering URLs, methods, errors, pagination, and idempotency.

## Prompt

Review this API design for REST best practices:

[paste your API routes/endpoints]

Evaluate:
1. URL structure: Are resources plural nouns? Proper nesting depth (max 2 levels)?
2. HTTP methods: Correct verb usage (GET/POST/PUT/PATCH/DELETE)?
3. Status codes: Appropriate codes for each response scenario?
4. Pagination: Cursor-based vs offset? Include total count?
5. Filtering/sorting: Query parameter conventions?
6. Error format: Consistent error response schema with machine-readable codes?
7. Versioning: URL path vs header vs query param?
8. Idempotency: Are POST/PUT operations idempotent where they should be?
9. HATEOAS: Are related resource links included?

For each issue found, provide the current design, what's wrong, and the corrected version.

## Tips

Catches common API anti-patterns before they become breaking changes.
