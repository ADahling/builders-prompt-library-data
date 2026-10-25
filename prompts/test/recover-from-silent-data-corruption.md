---
title: "Recover from Silent Data Corruption"
slug: recover-from-silent-data-corruption
stage: Test
category: "Critical Bugs"
grade: C
score: 67
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/recover-from-silent-data-corruption
---
# Recover from Silent Data Corruption

Audit, reprocess, and implement automated reconciliation to remediate silent ETL data corruption and prevent future financial reporting errors.

## Prompt

You are a data engineer. You have discovered that a critical dataset in your data warehouse has been silently corrupted for weeks. The corruption is subtle (e.g., incorrect calculations in a financial report) and was not caught by your existing data quality checks. Your task is to assess the damage and restore the data.

Context:
- The data warehouse is built on a technology like Snowflake or BigQuery.
- The corruption was introduced by a bug in an ETL (Extract, Transform, Load) job.
- The incorrect data has been used in several important business reports.

Provide:
1. A strategy to identify the exact source and timeframe of the corruption by analyzing the ETL job's code and history.
2. A plan to reprocess the historical data to fix the corrupted records in the data warehouse.
3. A proposal for more robust data quality checks and reconciliation processes to detect such silent corruption in the future.

## Tips

A challenging data integrity problem with significant business impact.
