---
title: "dbt Model Design Pattern"
slug: dbt-model-design-pattern
stage: Build
category: "Modern Data Stack"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/dbt-model-design-pattern
---
# dbt Model Design Pattern

Architect a production-ready dbt modeling layer featuring staging, logic, and mart layers with full testing and performance optimizations.

Variables: data_domain, warehouse_type, source_1_description, source_2_description, business_requirement_1, business_requirement_2

## Prompt

You are a senior analytics engineer. Design a dbt model architecture for {{data_domain}} in our {{warehouse_type}} data warehouse.

Source data:
- {{source_1_description}}
- {{source_2_description}}

Business requirements:
- {{business_requirement_1}}
- {{business_requirement_2}}

Provide:
1. **Staging Models**: One per source, with column renaming, type casting, and basic cleaning
2. **Intermediate Models**: Business logic transformations, joins, aggregations
3. **Mart Models**: Final business-facing tables optimized for BI tools
4. **Model DAG**: Show the dependency graph
5. **Testing Strategy**: schema.yml with tests for each model (unique, not_null, accepted_values, relationships)
6. **Documentation**: Model descriptions, column descriptions, business definitions
7. **Materialization Strategy**: View vs table vs incremental for each model
8. **Performance**: Partitioning, clustering, and query optimization

## Tips

Follow the dbt best practices: staging -> intermediate -> marts. Never skip the staging layer.
