---
title: "Implement JWT Authentication Middleware in a Node.js Application"
slug: implement-jwt-authentication-middleware-in-a-node-js-application
stage: Build
category: "API Design"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-jwt-authentication-middleware-in-a-node-js-application
---
# Implement JWT Authentication Middleware in a Node.js Application

Secure Node.js API endpoints by implementing JWT authentication middleware for token verification, payload decoding, and route protection.

Variables: framework

## Prompt

You are a backend security expert. I am building a Node.js application using the {{framework}} framework and I need to secure my API endpoints using JSON Web Tokens (JWT). Please provide a detailed guide on how to create and use a JWT authentication middleware.

**Requirements:**

1.  **JWT Creation:** Show how to generate a JWT when a user logs in or signs up. The token payload should include user information like 'userId' and 'role'. Use the 'jsonwebtoken' library.
2.  **Middleware Function:** Create a middleware function that can be applied to protected routes. This function should:
    *   Extract the JWT from the 'Authorization' header (Bearer Token scheme).
    *   Verify the token's signature and expiration date.
    *   If the token is valid, decode the payload and attach the user information to the request object (e.g., 'req.user').
    *   If the token is invalid or missing, send an appropriate error response (e.g., 401 Unauthorized).
3.  **Route Protection:** Demonstrate how to apply the middleware to protect specific routes in the application.
4.  **Best Practices:** Include a section on JWT security best practices, such as using a strong secret key, setting a short expiration time, and not storing sensitive information in the payload.

**Output Format:**
Provide the complete code for the authentication service and the middleware in a clear, commented TypeScript or JavaScript format. Include an example of a protected route.
