---
title: "GraphQL Schema Design Best Practices"
slug: graphql-schema-design-best-practices
stage: Build
category: "API Design"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/graphql-schema-design-best-practices
---
# GraphQL Schema Design Best Practices

Architect a scalable, production-ready GraphQL schema featuring Relay pagination, field-level security, and N+1 optimization for complex domains.

Variables: domain_name, entity_list, relationship_description, realtime_features

## Prompt

You are a GraphQL architect. Design a production-grade GraphQL schema for {{domain_name}}.

Domain entities:
{{entity_list}}

Relationships:
{{relationship_description}}

Design:
1. **Type Definitions**: All types with descriptions and deprecation notices
2. **Query Design**: Efficient queries with proper pagination (Relay cursor-based)
3. **Mutation Design**: Input types, payload types, error handling
4. **Subscription Design**: Real-time updates for {{realtime_features}}
5. **N+1 Prevention**: DataLoader patterns for each relationship
6. **Authorization**: Field-level authorization directives
7. **Complexity Analysis**: Query complexity limits and depth limits
8. **Caching Strategy**: Cache hints, persisted queries
9. **Federation**: How to split into subgraphs if needed
10. **Versioning**: How to evolve the schema without breaking clients

## Tips

A well-designed GraphQL schema is self-documenting and prevents the over-fetching problem of REST.
