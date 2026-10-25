---
title: "Progressive API Design (RESTful)"
slug: progressive-api-design-restful
stage: Build
category: "API Design"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/progressive-api-design-restful
---
# Progressive API Design (RESTful)

Design a REST API in stages, starting with core resources, relationships, attributes, and CRUD operations for your domain.

## Prompt

I'm designing a RESTful API for a [SPECIFIC DOMAIN] system.
Let's develop this progressively:

STAGE 1: Core resource definition
- Define the essential resources and their relationships
- Specify primary attributes for each resource
- Outline basic CRUD operations

STAGE 2: Interaction patterns
- Define specialized endpoints beyond CRUD
- Specify query parameters and filtering capabilities
- Design pagination and sorting approaches

STAGE 3: Advanced considerations
- Authentication and authorization patterns
- Rate limiting and quota strategies
- Caching directives and ETag implementation
- Versioning approach
- Error handling standardization (error format, codes)

STAGE 4: Documentation and examples
- Generate OpenAPI specifications
- Provide example requests/responses for common operations
- Document best practices for API consumers

Let's start with Stage 1 using these details:
[YOUR SPECIFIC API DOMAIN DETAILS, BUSINESS RULES, AND CLIENT USE CASES]

## Tips

Progressive design prevents the common mistake of trying to design everything at once. Source: medium.com/@onix_react/ultimate-prompts-for-every-developer
