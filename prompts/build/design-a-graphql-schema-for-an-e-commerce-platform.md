---
title: "Design a GraphQL Schema for an E-commerce Platform"
slug: design-a-graphql-schema-for-an-e-commerce-platform
stage: Build
category: "API Design"
grade: B
score: 78
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-graphql-schema-for-an-e-commerce-platform
---
# Design a GraphQL Schema for an E-commerce Platform

Design an e-commerce GraphQL schema with product, category, user, and order types, plus queries, mutations, inputs, and relationships.

Variables: id

## Prompt

Design a GraphQL schema for an e-commerce platform. The schema should include types for {Product}, {Category}, {User}, and {Order}. Define the following:
- Queries for retrieving product lists, products by {{id}}, and categories.
- Mutations for adding products to the cart, placing orders, and updating user profiles.
- Input types for mutations, including {ProductInput} for creating or updating products. 
- Relationships between types, such as a user having multiple orders and a product belonging to a category.

## Tips

This prompt is designed to help you think through the structure and relationships in your GraphQL API.
