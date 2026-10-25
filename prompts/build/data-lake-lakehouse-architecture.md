---
title: "Data Lake & Lakehouse Architecture"
slug: data-lake-lakehouse-architecture
stage: Build
category: "Modern Data Stack"
grade: A
score: 88
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/data-lake-lakehouse-architecture
---
# Data Lake & Lakehouse Architecture

Compare data lake, lakehouse, and warehouse architectures and table formats for your organization's data volume, use cases, cloud, and budget.

Variables: org_size, volume, uses, cloud, budget

## Prompt

# Data Lake & Lakehouse Architecture

## Context
- Organization size: {{org_size}}
- Data volume: {{volume}} (GB/TB/PB)
- Primary use cases: {{uses}} (analytics / ML / reporting / compliance)
- Cloud provider: {{cloud}} (AWS / GCP / Azure / multi-cloud)
- Budget: {{budget}}

## Architecture Options

### 1. Traditional Data Lake
```
Sources → Ingestion → Object Storage (S3/GCS/ADLS)
                          ↓
                    Query Engine (Athena/BigQuery/Presto)
                          ↓
                    Consumers (BI tools, notebooks)
```
**Pros:** Cheapest storage, schema-on-read flexibility
**Cons:** No ACID, no time travel, "data swamp" risk

### 2. Lakehouse (Recommended)
```
Sources → Ingestion → Table Format (Delta Lake / Apache Iceberg / Hudi)
                          ↓
                    on Object Storage (S3/GCS)
                          ↓
                    Query Engine (Spark, Trino, DuckDB)
                          ↓
                    Consumers
```
**Pros:** ACID transactions, time travel, schema evolution, cheap storage
**Cons:** More complex setup than pure warehouse

### 3. Cloud Data Warehouse
```
Sources → ELT Tool → Warehouse (BigQuery / Snowflake / Redshift)
                          ↓
                    dbt transforms
                          ↓
                    BI Tools
```
**Pros:** Simplest, fastest to set up, great SQL support
**Cons:** Expensive at scale, vendor lock-in

## Table Format Comparison
| Feature | Delta Lake | Apache Iceberg | Apache Hudi |
|---------|-----------|----------------|-------------|
| ACID Transactions | ✅ | ✅ | ✅ |
| Time Travel | ✅ | ✅ | ✅ |
| Schema Evolution | ✅ | ✅ (best) | ✅ |
| Partition Evolution | Manual | ✅ (hidden partitioning) | Manual |
| Engine Support | Spark-first | Multi-engine (best) | Spark, Flink |
| Community | Databricks-driven | Broad (Netflix, Apple) | Uber-driven |
| Catalog | Unity Catalog | REST Catalog, Hive | Hive |

## Implementation Checklist

### Storage Organization
```
s3://data-lake/
├── bronze/          # Raw, immutable
│   ├── source_a/
│   │   └── year=2026/month=03/
│   └── source_b/
├── silver/          # Cleaned, typed, deduplicated
│   ├── customers/
│   └── orders/
├── gold/            # Business aggregates
│   ├── daily_revenue/
│   └── customer_360/
└── sandbox/         # Exploration, temporary
```

### Governance
- [ ] Data catalog (DataHub, OpenMetadata, or cloud-native)
- [ ] Column-level lineage tracking
- [ ] PII detection and masking (automated scanning)
- [ ] Access control: role-based, column-level where needed
- [ ] Retention policies enforced automatically
- [ ] Cost allocation tags on all storage and compute

### Performance
- [ ] Partitioning strategy aligned with query patterns
- [ ] File compaction job (small files → optimal size 128-256MB)
- [ ] Statistics collection for query optimization
- [ ] Caching layer for hot data (Redis, Alluxio)
- [ ] Query result caching for repeated reports

### For Small Teams (< 10 engineers)
Skip the full lakehouse. Use:
1. **Supabase/Postgres** as operational DB
2. **dbt** for transforms (SQL, version-controlled)
3. **Metabase or Superset** for dashboards
4. **DuckDB** for ad-hoc analysis on exported Parquet files
5. Scale to lakehouse only when Postgres can't handle the volume

## Tips

Data lake and lakehouse architecture comparison with table format selection, storage organization, governance checklist, and small-team pragmatic recommendations.
