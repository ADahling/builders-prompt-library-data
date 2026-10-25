---
title: "Design an API for a Translation Service"
slug: design-an-api-for-a-translation-service-name-translation-service
stage: Build
category: "API Design"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-translation-service-name-translation-service
---
# Design an API for a Translation Service

Get a translation service API design with text translation and supported-language endpoints, plus a usage tracking mechanism for billing.

Variables: translation_service_name

## Prompt

I am building a translation service called {{translation_service_name}}. I need to design the API for it.

Your task is to design the core API for the service.

**Instructions:**
1.  **Translation Endpoint:** Design a simple API endpoint that takes a text and a target language as input and returns the translated text.
2.  **Supported Languages:** Design an API endpoint that returns a list of supported languages.
3.  **Usage Tracking:** Design a mechanism to track API usage (e.g., number of translated characters) for billing purposes.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoint, including the HTTP method, URI, and request/response format.
