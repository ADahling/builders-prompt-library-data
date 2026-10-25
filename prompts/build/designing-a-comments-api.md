---
title: "Designing a Comments API"
slug: designing-a-comments-api
stage: Build
category: "API Design"
grade: B
score: 71
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-comments-api
---
# Designing a Comments API

Design a RESTful API for post or article comments, with filtered retrieval, creation, deletion, response formats, and error handling.

Variables: content

## Prompt

Create a RESTful API for managing comments on {posts/articles}. Include endpoints for:
- {GET /comments}: Retrieving comments with optional filtering by {postId} or {userId}.
- {POST /comments}: Adding a new comment with fields {postId}, {userId}, and {{content}}.
- {DELETE /comments/{commentId}}: Deleting a specific comment. Define response formats and error handling.

## Tips

This prompt will help you implement a fundamental commenting feature in your application.
