---
title: "Diagnose Performance Degradation from Index Fragmentation"
slug: diagnose-performance-degradation-from-index-fragmentation
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/diagnose-performance-degradation-from-index-fragmentation
---
# Diagnose Performance Degradation from Index Fragmentation

Identify and resolve SQL Server performance issues by auditing index fragmentation via DMVs and implementing automated maintenance scripts.

## Prompt

You are a database administrator for a high-transaction SQL Server database. Over time, you have noticed that queries that used to be fast are now becoming slow, even though the query plans have not changed. You suspect that the database indexes have become fragmented. Your task is to diagnose and fix the fragmentation.

Context:
- The database has many tables with frequent inserts, updates, and deletes.
- This causes the logical order of pages in the indexes to differ from the physical order on disk (external fragmentation) and free space to appear on the index pages (internal fragmentation).
- You have access to SQL Server’s Dynamic Management Views (DMVs).

Provide:
1. A SQL query that uses the `sys.dm_db_index_physical_stats` DMV to check the fragmentation level of all indexes in the database.
2. An explanation of the difference between rebuilding and reorganizing an index, and when to use each one. (Rebuild is offline and creates a new, clean index; Reorganize is online and defragments the leaf level). 
3. A maintenance plan script that regularly checks for fragmentation and either rebuilds or reorganizes indexes based on their fragmentation level (e.g., reorganize if > 10%, rebuild if > 30%).

## Tips

A deep DBA topic that requires knowledge of database internals and maintenance.
