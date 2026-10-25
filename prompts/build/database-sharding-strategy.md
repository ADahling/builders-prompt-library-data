---
title: "Database Sharding Strategy"
slug: database-sharding-strategy
stage: Build
category: "System Architecture"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/database-sharding-strategy
---
# Database Sharding Strategy

Design and implement a scalable database sharding architecture to resolve performance bottlenecks and ensure seamless high-volume growth.

Variables: application_name, current_data_size, primary_table, growth_rate, pain_point_1, pain_point_2

## Prompt

You are a database architect. Design a sharding strategy for {{application_name}} that currently has {{current_data_size}} of data in {{primary_table}} and is growing at {{growth_rate}}.

Current pain points:
- {{pain_point_1}}
- {{pain_point_2}}

Provide:
1. **Shard Key Selection**: Analyze candidate shard keys and recommend one with justification
2. **Sharding Scheme**: Range-based, hash-based, or directory-based? Why?
3. **Migration Plan**: Zero-downtime migration from single DB to sharded architecture
4. **Cross-Shard Queries**: How to handle queries that span multiple shards
5. **Rebalancing Strategy**: How to add new shards without downtime
6. **Consistency Model**: How to maintain referential integrity across shards
7. **Monitoring**: Key metrics and alerts for shard health

## Tips

Critical for applications hitting single-database scaling limits. The shard key selection is the most important decision.
