---
title: "OpenAPI Spec Generator"
slug: openapi-spec-generator
stage: Build
category: "API Design"
grade: A
score: 88
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openapi-spec-generator
---
# OpenAPI Spec Generator

Write an OpenAPI 3.1 YAML spec for your API with shared schemas, examples, error responses, pagination, filtering, rate limit headers, and environments.

## Prompt

Generate a complete OpenAPI 3.1 specification for this API:

Service: [name and purpose]
Base URL: [base URL]
Auth: [auth method — Bearer, API key, OAuth2]

Endpoints:
[list your endpoints with brief descriptions]

Requirements:
1. Include request/response schemas with examples for every endpoint.
2. Use `$ref` for shared schemas (avoid duplication).
3. Add proper error responses (400, 401, 403, 404, 422, 500) with consistent format.
4. Include pagination parameters where applicable.
5. Add rate limiting headers (X-RateLimit-Limit, X-RateLimit-Remaining).
6. Document query parameters for filtering and sorting.
7. Add tags for logical grouping.
8. Include server environments (dev, staging, prod).

Output valid YAML.

## Tips

Produces spec files ready for Swagger UI, Redoc, or code generation.
