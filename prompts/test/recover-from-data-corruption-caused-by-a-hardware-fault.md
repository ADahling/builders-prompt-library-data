---
title: "Recover from Data Corruption Caused by a Hardware Fault"
slug: recover-from-data-corruption-caused-by-a-hardware-fault
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/recover-from-data-corruption-caused-by-a-hardware-fault
---
# Recover from Data Corruption Caused by a Hardware Fault

Restore a corrupted PostgreSQL instance by securing damaged data and performing point-in-time recovery using backups and WAL files.

## Prompt

You are a site reliability engineer. A critical database server has experienced a hardware fault (e.g., a faulty disk controller) that has led to data corruption on disk. The database will not start, and you need to recover the data with minimal loss.

Context:
- The database is a self-hosted PostgreSQL instance on a Linux server.
- The file system is reporting I/O errors when trying to read some of the database files.
- You have nightly backups and continuous archiving of WAL (Write-Ahead Logging) files to a remote storage location.

Provide:
1. An emergency plan to assess the extent of the corruption and secure the existing data files and WAL segments.
2. A detailed, step-by-step guide for performing a point-in-time recovery (PITR). This involves setting up a new server, restoring the last known good backup, and then replaying the WAL files up to the point just before the corruption occurred.
3. A proposal for improving the high availability of the database, such as setting up a streaming replication standby server to allow for a fast failover in the future.

## Tips

A worst-case scenario for a database administrator that requires deep knowledge of backup and recovery procedures.
