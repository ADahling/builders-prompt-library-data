---
title: "Recover from Data Corruption in an Elasticsearch Index"
slug: recover-from-data-corruption-in-an-elasticsearch-index
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/recover-from-data-corruption-in-an-elasticsearch-index
---
# Recover from Data Corruption in an Elasticsearch Index

Diagnose and recover a corrupted Elasticsearch index using API health checks and snapshot restoration to ensure search service availability.

## Prompt

You are a search engineer. An Elasticsearch index that backs a critical search feature has become corrupted. Some shards are in an unassigned state, and the cluster health is red. Your task is to recover the index with minimal data loss.

Context:
- The Elasticsearch cluster has multiple nodes.
- The corruption might have been caused by a sudden node failure or a disk issue.
- You have nightly snapshots of the cluster stored in a remote repository (like S3).

Provide:
1. A set of Elasticsearch API calls to diagnose the state of the cluster and the corrupted index (e.g., `_cluster/health`, `_cat/shards`, `_cluster/allocation/explain`).
2. A recovery plan. If the corrupted shards cannot be recovered, you will need to delete the index and restore it from the last known good snapshot. You will have to accept the loss of any data indexed since the last snapshot.
3. A recommendation for improving the resilience of the index, such as increasing the number of replica shards to provide more redundancy.

## Tips

A practical disaster recovery scenario for a popular search and analytics engine.
