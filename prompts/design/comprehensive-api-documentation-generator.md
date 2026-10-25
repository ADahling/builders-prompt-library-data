---
title: "Comprehensive API Documentation Generator"
slug: comprehensive-api-documentation-generator
stage: Design
category: "Documentation"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/comprehensive-api-documentation-generator
---
# Comprehensive API Documentation Generator

Comprehensive API Documentation Generator Scan a codebase or OpenAPI spec and produce clean, developer-facing API documentation.

## Prompt

# Comprehensive API Documentation Generator

Scan a codebase or OpenAPI spec and produce clean, developer-facing API documentation.

## Input
Provide ONE of:
- Codebase path (supports Express.js, FastAPI, Flask, and other frameworks)
- OpenAPI / Swagger spec
- Endpoint list (paste routes manually)

## Step 1 — Extraction
- Parse source files to find route definitions (e.g., @app.route('/users', methods=['GET']))
- Extract: endpoint path, HTTP method(s), request/response models or schemas
- Analyze function signatures for path parameters, query parameters, request body structures
- Look for comments or docstrings preceding route definitions for descriptions

## Step 2 — Documentation per Endpoint
For each endpoint, generate:
1. **Title** and one-line description
2. **HTTP method + URL path** (e.g., GET /users/{id})
3. **Authentication requirements** (Bearer token, API key, none)
4. **Parameters** — path, query, body — with name, type, required/optional status (use tables)
5. **Request** — headers, body schema with example JSON
6. **Response** — status codes with example JSON for success AND error cases
7. **Rate limits** if applicable
8. **Code examples** in cURL + JavaScript (fetch)
9. **Common errors** and troubleshooting tips

## Step 3 — Organization
- Group endpoints by resource (e.g., all /users endpoints together)
- Add table of contents with anchor links
- Use collapsible sections for lengthy examples
- Add "Try it" suggestions where applicable
- Note breaking changes from previous versions

## Output Formats
- Single Markdown file with complete API documentation
- Optionally host as static HTML using Slate, ReDoc, or Docusaurus

Write for a developer who has never seen this API before.

## Tips

Comprehensive API docs generator — combines codebase scanning with manual spec input. Merged from OpenClaw API Documentation Generator and API Documentation Writer.
