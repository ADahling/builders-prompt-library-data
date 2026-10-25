---
title: "Write Integration Tests for a REST API with Authentication"
slug: write-integration-tests-for-a-rest-api-with-authentication
stage: Test
category: "Testing & QA"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-integration-tests-for-a-rest-api-with-authentication
---
# Write Integration Tests for a REST API with Authentication

Write REST API integration tests covering valid logins, invalid credentials, missing or expired tokens, and role-based access to protected resources.

Variables: api_docs_url, auth_method, test_framework

## Prompt

I have a REST API with endpoints that require authentication. I need to write integration tests to verify that the authentication and authorization mechanisms are working correctly.

**Instructions:**
1.  **API Documentation:** The API is documented here: `{{api_docs_url}}`.
2.  **Authentication Method:** The API uses `{{auth_method}}` (e.g., JWT, OAuth 2.0).
3.  **Testing Framework:** Use `{{test_framework}}` (e.g., Supertest, Postman) to make HTTP requests to the API.
4.  **Test Scenarios:**
    *   **Successful Authentication:** Test that a valid user can obtain an authentication token and access protected endpoints.
    *   **Invalid Credentials:** Test that the API returns a `401 Unauthorized` error for incorrect login credentials.
    *   **Missing Token:** Test that protected endpoints return a `401 Unauthorized` error when no authentication token is provided.
    *   **Invalid or Expired Token:** Test that the API correctly handles invalid or expired tokens.
    *   **Authorization:** For different user roles, test that they can only access the endpoints and resources they are permitted to.
5.  **Output Format:** Provide the complete test script. The script should be organized with clear test descriptions. Sensitive data like API keys or passwords should be handled securely (e.g., using environment variables).
