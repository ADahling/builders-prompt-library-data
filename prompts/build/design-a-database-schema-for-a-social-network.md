---
title: "Design a Database Schema for a Social Network"
slug: design-a-database-schema-for-a-social-network
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-database-schema-for-a-social-network
---
# Design a Database Schema for a Social Network

Design a social network database schema for users, relationships, and posts, with feed generation queries and scaling strategies.

Variables: database_type

## Prompt

I am designing a social network application, and I need to create a database schema to store the user data, the social graph (i.e., the relationships between users), and the posts that users create. The schema needs to be scalable and performant. Our database is {{database_type}}.

Your task is to design a database schema for the social network. The design should include:

1.  **User Table:** A table to store the user data, such as the user's name, email address, and profile picture.
2.  **Social Graph:** A design for how to represent the social graph. This could involve using a self-referencing table to store the relationships between users or using a graph database.
3.  **Post Table:** A table to store the posts that users create. The table should include the post's content, the user who created it, and the timestamp.
4.  **Feed Generation:** A plan for how to generate a user's feed, which is a list of posts from the users they follow. This should be a performant query that can scale to a large number of users and posts.
5.  **Scalability:** A discussion of how to scale the database schema as the social network grows. This could involve using techniques like sharding and caching.

## Tips

This prompt is a common design problem for developers building social applications.
