---
title: "Design a GraphQL Schema for a Real-time Chat Application"
slug: design-a-graphql-schema-for-a-real-time-chat-application
stage: Build
category: "API Design"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-graphql-schema-for-a-real-time-chat-application
---
# Design a GraphQL Schema for a Real-time Chat Application

Architect a complete GraphQL schema with types, queries, and subscriptions to enable real-time messaging and room management features.

## Prompt

You are a GraphQL specialist. Design a GraphQL schema for a real-time chat application. The application will have users, chat rooms, and messages. The schema should support real-time updates using GraphQL Subscriptions.

**Features to support:**

*   Users can join and leave chat rooms.
*   Users can send and receive messages in real-time.
*   The application should show a list of users currently in a chat room.
*   Users can view the message history of a chat room.

**Requirements:**
1.  **Types:** Define the GraphQL types for ‘User’, ‘ChatRoom’, and ‘Message’.
2.  **Queries:** Define queries to fetch chat rooms, messages in a room, and the current user.
3.  **Mutations:** Define mutations for sending a message, creating a chat room, and joining/leaving a room.
4.  **Subscriptions:** Define a subscription to listen for new messages in a specific chat room.

**Output Format:**
Provide the complete GraphQL schema in a single code block using GraphQL Schema Definition Language (SDL). Add comments to explain the purpose of each type, query, mutation, and subscription.
