---
title: "Designing an API for a Blogging Platform"
slug: designing-an-api-for-a-blogging-platform
stage: Build
category: "API Design"
grade: B
score: 76
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-an-api-for-a-blogging-platform
---
# Designing an API for a Blogging Platform

Design a blogging API for listing, creating, reading, updating, and deleting posts, with author or tag filters, responses, and status codes.

Variables: author, tag, title, content

## Prompt

Design a RESTful API for a blogging platform. Include endpoints for:
- {GET /posts}: Retrieve a list of blog posts with optional filtering by {{author}} or {{tag}}.
- {POST /posts}: Create a new blog post with the fields {{title}}, {{content}}, and {authorId}.
- {GET /posts/{postId}}: Retrieve details of a specific blog post.
- {PUT /posts/{postId}}: Update an existing post by {postId}.
- {DELETE /posts/{postId}}: Delete a blog post. Define response formats and status codes.

## Tips

This prompt will help you create a foundational API for content management.
