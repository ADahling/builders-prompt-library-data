---
title: "Design a Standardized API Error Handling and Response Format"
slug: design-a-standardized-api-error-handling-and-response-format
stage: Build
category: "API Design"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-standardized-api-error-handling-and-response-format
---
# Design a Standardized API Error Handling and Response Format

Standardize API error handling by designing a uniform JSON response format, custom error classes, and global middleware for a given framework.

Variables: framework

## Prompt

You are a principal software engineer. Our development team is growing, and our API, which is built with {{framework}}, has inconsistent error handling. Different endpoints return errors in different formats, which makes it difficult for client-side developers to handle them properly. I want to establish a standardized approach to error handling.

**Task:**
Design a standardized error response format for our API and create a global error handling middleware to enforce it.

**Requirements:**

1.  **Error Response Format:**
    *   Design a consistent JSON error response format. It should include a unique error code, a human-readable message, and optionally, a field for validation errors.
    *   Provide examples of what the error response would look like for different types of errors (e.g., resource not found, validation failed, internal server error).
2.  **Custom Error Classes:**
    *   Show how to create custom error classes (e.g., 'NotFoundError', 'ValidationError') that extend the base 'Error' class. This will help in creating more structured and predictable error handling logic.
3.  **Global Error Handler:**
    *   Provide the code for a global error handling middleware in our framework. This middleware should catch all errors that occur in the application, log them, and then send a response to the client in the standardized format you designed.

**Output Format:**
Provide a Markdown document that specifies the error format. Include the code for the custom error classes and the global error handling middleware in a well-commented code block.
