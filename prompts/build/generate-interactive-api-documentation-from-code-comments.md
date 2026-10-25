---
title: "Generate Interactive API Documentation from Code Comments"
slug: generate-interactive-api-documentation-from-code-comments
stage: Build
category: "API Design"
grade: A
score: 88
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-interactive-api-documentation-from-code-comments
---
# Generate Interactive API Documentation from Code Comments

Automate the creation of interactive, auto-updating API documentation by extracting OpenAPI specifications from source code annotations.

Variables: framework

## Prompt

You are a developer advocate. My team has built a REST API using {{framework}}, but our documentation is manually written and often out of date. I want to automate the generation of our API documentation directly from our source code to ensure it's always accurate. The documentation should be interactive, like what you see with Swagger UI or Redoc.

**Task:**
Provide a step-by-step guide on how to use a tool to generate interactive API documentation from code comments or annotations.

**Instructions:**

1.  **Tool Selection:** Recommend a suitable tool for our tech stack (e.g., Swagger/OpenAPI with JSDoc for Node.js, or similar tools for other languages). Justify your choice.
2.  **Code Annotation:** Show how to annotate our route handlers and data models with comments that the tool can parse. The annotations should describe the endpoint, its parameters, request body, and possible responses.
3.  **Documentation Generation:** Explain the process of running the tool to generate the OpenAPI specification file (e.g., 'swagger.json').
4.  **UI Setup:** Show how to set up a documentation UI (like Swagger UI) that uses the generated specification file to display interactive documentation where users can try out the API endpoints directly from their browser.

**Output Format:**
Write the guide in Markdown. Include clear code examples of the annotated routes and the script to generate the documentation.
