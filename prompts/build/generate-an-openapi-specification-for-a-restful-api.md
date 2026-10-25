---
title: "Generate an OpenAPI Specification for a RESTful API"
slug: generate-an-openapi-specification-for-a-restful-api
stage: Build
category: "API Design"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-an-openapi-specification-for-a-restful-api
---
# Generate an OpenAPI Specification for a RESTful API

Get an OpenAPI 3.0 YAML specification for your REST API's CRUD endpoints, including metadata, parameters, request bodies, responses, and schemas.

Variables: domain, resource_plural, resource_singular

## Prompt

I have designed a RESTful API for a {{domain}} application. Now I need to create an OpenAPI 3.0 specification for it to serve as documentation and to be used for generating client SDKs.

The API has the following endpoints:
*   `GET /{{resource_plural}}`
*   `POST /{{resource_plural}}`
*   `GET /{{resource_plural}}/{id}`
*   `PUT /{{resource_plural}}/{id}`
*   `DELETE /{{resource_plural}}/{id}`

Your task is to generate the OpenAPI 3.0 specification for this API in YAML format.

**Instructions:**
1.  **Info Object:** Define the `info` object with the title, description, and version of the API.
2.  **Paths Object:** Define the `paths` object with the five endpoints listed above. For each endpoint, specify the HTTP method, a summary, a description, parameters (if any), request body (if any), and possible responses (including success and error responses).
3.  **Components Object:** Define the `components` object with the schema for the `{{resource_singular}}` resource.

**Output Format:**
Provide the output as a single block of YAML code representing the OpenAPI 3.0 specification.
