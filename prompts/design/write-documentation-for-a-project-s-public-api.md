---
title: "Write Documentation for a Project's Public API"
slug: write-documentation-for-a-project-s-public-api
stage: Design
category: "Documentation"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-documentation-for-a-project-s-public-api
---
# Write Documentation for a Project's Public API

Write Markdown documentation for a public API endpoint, including its method, purpose, parameter tables, and applicable request body examples.

Variables: project_name, endpoint_path, http_method, endpoint_purpose

## Prompt

I have an open-source project, `{{project_name}}`, that exposes a public API. I need to write clear, comprehensive, and user-friendly documentation for one of its core API endpoints.

**Endpoint**: `{{endpoint_path}}` (e.g., `/api/v1/users/{id}`)
**HTTP Method**: `{{http_method}}` (e.g., GET, POST)
**Purpose**: `{{endpoint_purpose}}` (e.g., Retrieves a specific user's profile)

Generate the complete Markdown documentation for this specific API endpoint. The documentation should be structured in a standard format, suitable for inclusion in a larger API documentation site or a project's README.

The documentation must include:

1.  **Endpoint Title and Method**: A clear heading with the HTTP method and path.
    *   Example: `## GET /api/v1/users/{id}`
2.  **Description**: A brief paragraph explaining what the endpoint does.
3.  **Path Parameters**: A table describing any parameters in the URL path.
    *   Columns: `Parameter`, `Type`, `Description`, `Required`
    *   Example: `id`, `string`, "The unique identifier of the user.", `Yes`
4.  **Query Parameters (if any)**: A table for optional query parameters.
    *   Columns: `Parameter`, `Type`, `Description`, `Default`
    *   Example: `include_details`, `boolean`, "If true, includes extra user details.", `false`
5.  **Request Body (for POST/PUT/PATCH)**: If the endpoint accepts a request body, provide a description and a JSON example.
    *   Specify the `Content-Type` (e.g., `application/json`).
    *   Provide a well-formatted JSON object showing the expected structure.
6.  **Responses**: A section detailing the possible HTTP responses.
    *   **Success Response (e.g., 200 OK)**: Describe the success condition and provide an example of the JSON response body.
    *   **Error Responses (e.g., 404 Not Found, 401 Unauthorized)**: Describe the conditions for each error and the structure of the error response body.
7.  **Example Request**: A complete example of how to call the API using a tool like `curl` or a language-specific library like Python's `requests`.

Constraint Checklist & Confidence Score:
1.  Is the documentation well-structured and easy to follow? Yes.
2.  Does it include all the required sections (parameters, request/response bodies, examples)? Yes.
3.  Are the examples clear and correct? Yes.
4.  Is the output in valid Markdown format? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the detailed API documentation for the specified endpoint.

## Tips

Clear API documentation is not a 'nice-to-have'; it is essential for the adoption and usability of any project that exposes an API.
