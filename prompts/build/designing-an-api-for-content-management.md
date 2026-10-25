---
title: "Designing an API for Content Management"
slug: designing-an-api-for-content-management
stage: Build
category: "API Design"
grade: B
score: 76
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-an-api-for-content-management
---
# Designing an API for Content Management

Design a CMS article API with list, create, read, update, and delete endpoints, category filtering, response structures, and status codes.

Variables: category, title, content

## Prompt

Create a RESTful API for a content management system (CMS). Include endpoints for:
- {GET /articles}: Retrieving a list of articles with optional filtering by {{category}}.
- {POST /articles}: Creating a new article with fields {{title}}, {{content}}, and {authorId}.
- {GET /articles/{articleId}}: Fetching details of a specific article.
- {PUT /articles/{articleId}}: Updating an article by {articleId}.
- {DELETE /articles/{articleId}}: Deleting an article. Define response structures and status codes.

## Tips

This prompt will help you set up a basic API for managing content.
