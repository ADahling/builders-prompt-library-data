---
title: "Design an API for a Social Network"
slug: design-an-api-for-a-social-network-name-social-network
stage: Build
category: "API Design"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-social-network-name-social-network
---
# Design an API for a Social Network

Get a RESTful API design for a social network, with endpoints for authentication, posts, comments, likes, friend requests, and a friends' news feed.

Variables: social_network_name

## Prompt

I am building a new social network called {{social_network_name}}. I need to design the API for it.

Your task is to design the core API for the social network.

**Instructions:**
1.  **Core Resources:** Identify the core resources of the social network (e.g., users, posts, comments, likes, friendships).
2.  **API Design:** Design the RESTful API endpoints for the following features:
    *   User registration and authentication.
    *   Creating, retrieving, updating, and deleting posts.
    *   Commenting on posts.
    *   Liking posts.
    *   Sending and accepting friend requests.
    *   A news feed that shows the posts from the user's friends.

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoints, including the HTTP methods, URIs, and request/response formats.
