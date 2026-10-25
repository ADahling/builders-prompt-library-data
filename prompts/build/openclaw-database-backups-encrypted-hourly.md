---
title: "OpenClaw: Database Backups \u2014 Encrypted Hourly"
slug: openclaw-database-backups-encrypted-hourly
stage: Build
category: "OpenClaw"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-database-backups-encrypted-hourly
---
# OpenClaw: Database Backups — Encrypted Hourly

Set up hourly encrypted SQLite backups to Google Drive with rolling retention, integrity checks, Telegram failure alerts, and a restore script.

## Prompt

# Database Backups — Encrypted Hourly

Set up an automated database backup system:

## Schedule
Cron: Every hour

## Pipeline
1. Auto-discover all SQLite databases in the project (no manual config — new databases get picked up automatically)
2. Bundle into an encrypted tar archive
3. Upload to Google Drive

## Retention
- Keep the last 7 backups (rolling window)
- Can restore to any point in the past week

## Restore Script
Include a full restore script that:
- Downloads the specified backup from Google Drive
- Decrypts the archive
- Restores databases to their original locations
- Validates integrity after restore

## Error Handling
- If any backup fails, alert immediately via Telegram
- Log backup sizes for anomaly detection (sudden size changes = potential issue)
- Verify backup integrity before uploading (test decryption)

## Security
- Encryption key stored in environment variable, never in code
- Backup files scrubbed of any plaintext credentials before archiving

## Tips

Hourly encrypted SQLite backup to Google Drive with auto-discovery, 7-day retention, and restore script. From mberman84's gist.
