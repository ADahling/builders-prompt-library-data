---
title: "Creating a RESTful API for User Profiles"
slug: creating-a-restful-api-for-user-profiles
stage: Build
category: "API Design"
grade: B
score: 79
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/creating-a-restful-api-for-user-profiles
---
# Creating a RESTful API for User Profiles

Design a user profile REST API with create, read, update, and delete endpoints, status filtering, response formats, and error handling.

Variables: status, name, email, password

## Prompt

Design a RESTful API for user profiles with these endpoints:
- {GET /users}: Retrieve a list of user profiles with optional filtering by {{status}}.
- {POST /users}: Create a new user profile with fields {{name}}, {{email}}, and {{password}}.
- {GET /users/{userId}}: Retrieve details for a specific user profile.
- {PUT /users/{userId}}: Update a user profile.
- {DELETE /users/{userId}}: Delete a user profile. Define response formats and error handling.

## Tips

This prompt will help you create a foundational user management system in your API.
