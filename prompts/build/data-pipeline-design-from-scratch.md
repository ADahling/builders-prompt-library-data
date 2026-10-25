---
title: "Data Pipeline Design from Scratch"
slug: data-pipeline-design-from-scratch
stage: Build
category: "Modern Data Stack"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/data-pipeline-design-from-scratch
---
# Data Pipeline Design from Scratch

Plan data pipeline ingestion, layered storage, and transformation tools around your sources, data volume, freshness needs, and consumers.

Variables: sources, volume, freshness, consumers

## Prompt

# Data Pipeline Architecture Design

## Requirements
- Data sources: {{sources}} (databases, APIs, event streams, files)
- Volume: {{volume}} (records/day or GB/day)
- Freshness: {{freshness}} (real-time / near-real-time / hourly / daily)
- Consumers: {{consumers}} (dashboards, ML models, APIs, reports)

## Architecture Layers

### 1. Ingestion
```
Sources → Ingestion Layer → Raw Storage
```

| Source Type | Tool | Pattern |
|-------------|------|---------|
| Databases | Debezium, Airbyte, Fivetran | CDC (Change Data Capture) |
| APIs | Airbyte, custom scripts | Scheduled polling or webhooks |
| Event streams | Kafka, Redpanda, Pub/Sub | Streaming ingestion |
| Files (CSV/JSON) | Cloud Functions, Airflow | File watcher + parser |
| SaaS (Stripe, HubSpot) | Fivetran, Airbyte | Pre-built connectors |

### 2. Storage (Medallion Architecture)
```
Bronze (Raw) → Silver (Cleaned) → Gold (Business-Ready)
```

| Layer | Purpose | Format | Retention |
|-------|---------|--------|-----------|
| Bronze | Raw, immutable, as-received | Parquet/JSON | 1-2 years |
| Silver | Deduplicated, typed, joined | Parquet (partitioned) | 1 year |
| Gold | Aggregated, business metrics | Parquet / materialized views | Indefinite |

### 3. Transformation
| Tool | Best For |
|------|----------|
| dbt | SQL transformations, version-controlled, tested |
| Apache Spark | Large-scale processing, ML feature engineering |
| Postgres functions | Simple transforms close to the database |
| Supabase Edge Functions | Real-time transforms on write |

### 4. Orchestration
| Tool | Best For |
|------|----------|
| Airflow / Dagster | Complex DAGs, Python-heavy |
| Prefect | Modern Python orchestration |
| dbt Cloud | SQL-only pipelines |
| GitHub Actions | Simple scheduled jobs |
| Cron + Edge Functions | Lightweight, serverless |

### 5. Serving
| Consumer | Serving Layer |
|----------|---------------|
| Dashboards | Data warehouse (BigQuery, Snowflake) or Postgres |
| APIs | Materialized views + REST/GraphQL |
| ML Models | Feature store (Feast, Tecton) |
| Real-time | Streaming output (Kafka → consumer) |
| Spreadsheets | Scheduled CSV/Google Sheets export |

## Quality & Observability
- [ ] Schema validation at ingestion (reject malformed early)
- [ ] Row count reconciliation (source vs destination)
- [ ] Freshness alerts (data older than SLA)
- [ ] Data quality tests in dbt (not_null, unique, accepted_values, relationships)
- [ ] Pipeline run monitoring (Dagster/Airflow UI or custom dashboard)
- [ ] Cost tracking per pipeline

## Tips

End-to-end data pipeline design covering ingestion, medallion storage, transformation, orchestration, and serving layers with tool recommendations.
