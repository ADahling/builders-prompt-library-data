---
title: "REST API Error Handling Standard"
slug: rest-api-error-handling-standard
stage: Build
category: "API Design"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/rest-api-error-handling-standard
---
# REST API Error Handling Standard

Establish a standardized, developer-friendly error handling framework that ensures consistent API responses and streamlined client-side debugging.

Variables: api_name

## Prompt

You are an API architect. Design a comprehensive error handling standard for the {{api_name}} REST API.

Requirements:
- Must be consistent across all endpoints
- Must be machine-readable and human-friendly
- Must support internationalization
- Must include enough detail for debugging without leaking internals

Design:
1. **Error Response Schema**: Standard JSON structure for all errors
2. **Error Code System**: Hierarchical error codes (e.g., AUTH_001, VALIDATION_002)
3. **HTTP Status Code Mapping**: Which errors map to which HTTP status codes
4. **Validation Errors**: How to return field-level validation errors
5. **Rate Limit Errors**: Headers and response body for rate limiting
6. **Retry Guidance**: Which errors are retryable and with what backoff
7. **Error Catalog**: Documentation page listing all possible errors
8. **Client-Side Handling**: TypeScript error handling utilities
9. **Logging Strategy**: What to log server-side for each error type
10. **Monitoring**: Error rate dashboards and alerting thresholds

## Tips

Good error handling is what separates amateur APIs from professional ones. Clients will thank you.
