---
title: "Data Validation Layer Design"
slug: data-validation-layer-design
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/data-validation-layer-design
---
# Data Validation Layer Design

Architect a resilient multi-tier validation strategy to ensure end-to-end data integrity and security across all application data flows.

Variables: application_name, input_sources, external_apis, database_tables

## Prompt

You are a backend architect. Design a comprehensive data validation layer for {{application_name}}.

Data flows:
- User input from {{input_sources}}
- External API data from {{external_apis}}
- Database reads from {{database_tables}}

Design:
1. **Input Validation**: Zod/Yup schemas for all user inputs
2. **API Response Validation**: Runtime type checking for external API responses
3. **Database Output Validation**: Ensuring DB queries return expected shapes
4. **Sanitization**: HTML sanitization, SQL escaping, path traversal prevention
5. **Business Rule Validation**: Domain-specific rules (e.g., date ranges, amount limits)
6. **Error Messages**: User-friendly validation error messages with field-level detail
7. **Validation Middleware**: Express/Fastify middleware for automatic request validation
8. **Client-Side Validation**: Shared validation schemas between frontend and backend
9. **Testing**: Unit tests for each validation schema
10. **Performance**: Validation caching, lazy validation for large payloads

## Tips

Never trust user input. Never trust external APIs. Never trust your own database. Validate everything.
