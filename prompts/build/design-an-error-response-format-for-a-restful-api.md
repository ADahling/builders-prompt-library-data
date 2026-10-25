---
title: "Design an Error Response Format for a RESTful API"
slug: design-an-error-response-format-for-a-restful-api
stage: Build
category: "API Design"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-error-response-format-for-a-restful-api
---
# Design an Error Response Format for a RESTful API

Get a standard JSON error schema for your RESTful API, at least five domain-specific error codes, and example responses for 400 and 404 errors.

## Prompt

I need to design a consistent and informative error response format for my RESTful API. When an error occurs, the API should return a JSON response that helps the client understand the problem.

Your task is to design a standardized error response format.

**Instructions:**
1.  **Error Schema:** Define the JSON schema for the error response. It should include fields like 'error_code', 'error_message', and 'error_details'.
2.  **Error Codes:** Create a list of at least 5 custom error codes for a specific domain (e.g., e-commerce, social media). For each error code, provide a clear description.
3.  **Example Responses:** Provide example error responses for a 400 (Bad Request) and a 404 (Not Found) error, using the schema you designed.

**Output Format:**
Provide the output as a Markdown document. Start with the JSON schema for the error response. Then, present the list of custom error codes in a table. Finally, show the example error responses in JSON format.
