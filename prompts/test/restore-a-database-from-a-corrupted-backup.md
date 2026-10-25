---
title: "Restore a Database from a Corrupted Backup"
slug: restore-a-database-from-a-corrupted-backup
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/restore-a-database-from-a-corrupted-backup
---
# Restore a Database from a Corrupted Backup

Recover lost data from corrupted MySQL backups by repairing dump files and performing point-in-time recovery using binary logs.

## Prompt

You are a database reliability engineer. The primary database has failed, and the latest backup file is found to be corrupted and cannot be restored directly. Your task is to recover the database to a consistent state.

Context:
- The database is MySQL, and backups are taken nightly using `mysqldump`.
- The corruption is in the middle of the SQL dump file, making it syntactically invalid.
- You have access to the binary logs (`binlogs`) from the server.

Provide:
1. A method to manually repair the corrupted `mysqldump` file to recover as much data as possible.
2. A plan to use point-in-time recovery with the last known good backup and the binary logs to restore the database to a state right before the failure.
3. Recommendations for improving the backup and verification strategy to prevent this from happening again.

## Tips

A practical and stressful scenario for a database engineer.
