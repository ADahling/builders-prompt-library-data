---
title: "API Documentation Generator (OpenAPI)"
slug: api-documentation-generator-openapi
stage: Design
category: "Documentation"
grade: A+
score: 90
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-documentation-generator-openapi
---
# API Documentation Generator (OpenAPI)

Generate comprehensive OpenAPI 3.1 specifications including endpoints, schemas, authentication guides, and multi-language code examples.

Variables: api_name, base_url, auth_method, endpoint_list

## Prompt

You are a technical writer specializing in API documentation. Generate comprehensive OpenAPI 3.1 documentation for the {{api_name}} API.

API details:
- Base URL: {{base_url}}
- Authentication: {{auth_method}}
- Endpoints: {{endpoint_list}}

For each endpoint, document:
1. **Summary and Description**: What it does and when to use it
2. **Parameters**: Path, query, header parameters with types and validation
3. **Request Body**: JSON schema with examples
4. **Response Codes**: 200, 201, 400, 401, 403, 404, 500 with example bodies
5. **Error Format**: Consistent error response schema
6. **Rate Limits**: Per-endpoint rate limit headers
7. **Code Examples**: cURL, JavaScript (fetch), Python (requests)
8. **Changelog**: Version history for breaking changes

Also provide:
- Getting Started guide (authentication, first API call)
- Pagination guide
- Webhook documentation
- SDK installation instructions

## Tips

Good API docs reduce support tickets by 50%. Use the OpenAPI spec to auto-generate SDKs and test suites.
