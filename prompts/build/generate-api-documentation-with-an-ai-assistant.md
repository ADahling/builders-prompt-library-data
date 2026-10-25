---
title: "Generate API Documentation with an AI Assistant"
slug: generate-api-documentation-with-an-ai-assistant
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-api-documentation-with-an-ai-assistant
---
# Generate API Documentation with an AI Assistant

Turn Node.js endpoint code into Markdown API documentation covering the path, HTTP method, purpose, request body, and success and error responses.

Variables: endpoint_code

## Prompt

You have a REST API endpoint defined in a Node.js application. Your task is to use an AI coding assistant to generate documentation for this endpoint in Markdown format.

Endpoint Code:
```javascript
{{endpoint_code}}
```

Generate documentation that includes:
1. The endpoint's path and HTTP method.
2. A brief description of what it does.
3. The structure of the request body.
4. The structure of the success and error responses.

## Tips

Automates the often tedious task of writing documentation.
