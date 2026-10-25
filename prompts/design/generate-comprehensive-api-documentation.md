---
title: "Generate Comprehensive API Documentation"
slug: generate-comprehensive-api-documentation
stage: Design
category: "Documentation"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-comprehensive-api-documentation
---
# Generate Comprehensive API Documentation

Produce professional-grade API documentation including technical specifications, JSON schema examples, and multi-language code snippets.

Variables: product_name

## Prompt

You are a senior technical writer tasked with creating comprehensive and user-friendly API documentation for our new {{product_name}}. The target audience is external developers with varying levels of experience. 

Your documentation should be structured logically and include the following sections for each endpoint:

*   **Endpoint:** The HTTP method and URL (e.g., POST /api/v1/users).
*   **Description:** A clear and concise explanation of the endpoint's purpose and functionality.
*   **Request Parameters:** A detailed list of all possible request parameters, including their data types, whether they are required or optional, and any validation rules or constraints.
*   **Request Body:** A sample request body in JSON format, with clear explanations for each field.
*   **Response Body:** A sample successful response body in JSON format, along with examples of possible error responses and their corresponding status codes.
*   **Code Examples:** Provide code examples in at least three popular programming languages (e.g., Python, JavaScript, Java) demonstrating how to make a request to the endpoint and handle the response.

Here is the technical specification for the first endpoint to document:

**Endpoint:** `POST /api/v1/projects`
**Description:** Creates a new project.
**Request Body:**
- `name` (string, required): The name of the project.
- `description` (string, optional): A brief description of the project.
- `is_public` (boolean, optional, default: false): Whether the project is public or private.

Generate the full documentation for this endpoint, following the structure and quality standards outlined above. Ensure the language is clear, concise, and easy to understand for developers of all skill levels.
