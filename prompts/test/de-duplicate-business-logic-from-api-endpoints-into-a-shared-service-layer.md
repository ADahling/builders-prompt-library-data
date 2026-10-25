---
title: "De-duplicate Business Logic from API Endpoints into a Shared Service Layer"
slug: de-duplicate-business-logic-from-api-endpoints-into-a-shared-service-layer
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 63
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/de-duplicate-business-logic-from-api-endpoints-into-a-shared-service-layer
---
# De-duplicate Business Logic from API Endpoints into a Shared Service Layer

Similar business logic is duplicated across multiple API endpoints in your backend service.

Variables: framework

## Prompt

In my `{{framework}}` backend application, I have noticed that similar business logic is duplicated across multiple API endpoints. For example, the logic for validating user permissions and then fetching some data is repeated in the `GET /items/:id

## Tips

This is a fundamental architectural refactoring for building scalable and maintainable backend applications.
