---
title: "GraphQL API Design and Security Audit"
slug: graphql-api-design-and-security-audit
stage: Test
category: "Quality Audits"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/graphql-api-design-and-security-audit
---
# GraphQL API Design and Security Audit

Conduct a comprehensive security and design audit of a GraphQL API to optimize schema architecture, authentication, and performance.

Variables: api_name, project_description, tech_stack

## Prompt

As a lead developer, I need a comprehensive audit of our GraphQL API, `{{api_name}}`. This API serves as the backbone for our {{project_description}} and is consumed by multiple client applications. The API is built with {{tech_stack}}. We need to ensure that our API is well-designed, secure, and easy to use.

Your audit should cover the following aspects of our API:

1.  **API Design and GraphQL Best Practices:**
    *   Evaluate the API's schema design, including the use of types, queries, mutations, and subscriptions.
    *   Assess the consistency and predictability of the API's design.
    *   Review the API's versioning strategy.

2.  **Data Formatting and Validation:**
    *   Analyze the request and response data formats for consistency and clarity.
    *   Review the input validation mechanisms to prevent common vulnerabilities like injection attacks and invalid data.

3.  **Authentication and Authorization:**
    *   Audit the authentication and authorization mechanisms to ensure they are secure and properly implemented.
    *   Check for any potential vulnerabilities, such as weak API keys or improper access control.

4.  **Performance and Scalability:**
    *   Analyze the API's response times and identify any performance bottlenecks.
    *   Review the use of pagination, caching, and rate limiting to ensure the API can scale to handle a large number of requests.

5.  **Documentation:**
    *   Review the API documentation for clarity, completeness, and accuracy.
    *   Ensure that the documentation provides clear examples of how to use the API.

**Output Format:**

Please provide an API audit report in a Markdown file with the following structure:

*   **API Health Score:** A summary of the API's overall quality, with scores for each of the audited areas.
*   **Audit Findings:** A detailed list of all identified issues, categorized by the areas mentioned above. For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **Severity:** (High, Medium, Low)
    *   **Description:** A clear explanation of the issue.
    *   **Recommendation:** Specific and actionable steps to fix the issue.
*   **API Improvement Roadmap:** A prioritized list of recommendations for improving the API's design, security, and performance.

Your report should provide our team with a clear and actionable plan for improving our API.
