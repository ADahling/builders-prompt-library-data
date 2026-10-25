---
title: "OpenClaw: API Contract & Schema Validator"
slug: openclaw-api-contract-schema-validator
stage: Build
category: "OpenClaw"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-api-contract-schema-validator
---
# OpenClaw: API Contract & Schema Validator

API Contract & Schema Validator Purpose Validate API contracts between frontend and backend to catch breaking changes before deployment.

## Prompt

# API Contract & Schema Validator

## Purpose
Validate API contracts between frontend and backend to catch breaking changes before deployment.

## Input
Provide:
- OpenAPI/Swagger spec (YAML or JSON)
- OR a before/after pair of specs for diff analysis
- OR sample request/response payloads

## Validation Checks

### Schema Validation
- All required fields present
- Type correctness (string, number, boolean, array, object)
- Enum values match spec
- Nullable fields properly annotated
- Default values specified where appropriate

### Breaking Change Detection
| Change | Breaking? | Action |
|--------|-----------|--------|
| Remove field | ✅ Yes | Block release |
| Rename field | ✅ Yes | Block release |
| Change type | ✅ Yes | Block release |
| Add required field | ✅ Yes | Block release |
| Add optional field | ❌ No | Log |
| Deprecate field | ⚠️ Maybe | Warn, require migration timeline |
| Change enum values | ✅ Yes | Block if removing values |

### Consistency Checks
- Naming conventions (camelCase vs snake_case)
- Pagination patterns (cursor vs offset)
- Error response format consistency
- Auth header requirements
- Rate limit header presence

## Output
1. ✅ Pass / ❌ Fail with specific violations
2. Breaking changes list with severity
3. Suggested fixes for each violation
4. Migration guide draft for breaking changes

## Tips

Validates API contracts and detects breaking changes between spec versions. Outputs violation reports and migration guides.
