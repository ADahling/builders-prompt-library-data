---
title: "OpenClaw: Self-Maintenance \u2014 Updates & Backups"
slug: openclaw-self-maintenance-updates-backups
stage: Build
category: "OpenClaw"
grade: C
score: 67
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-self-maintenance-updates-backups
---
# OpenClaw: Self-Maintenance — Updates & Backups

Set up daily OpenClaw updates and GitHub backups with secret scans, gateway restarts, and Discord reports for ongoing agent maintenance.

## Prompt

# Self-Maintenance: Auto-Updates & GitHub Backups

## Auto-Update (4:00 AM daily)
1. Run OpenClaw update command (package, gateway, all installed skills)
2. Restart the gateway service after update completes
3. Report results to Discord #monitoring channel:
   - What was updated
   - Any errors
   - Current version numbers
4. If something fails, report exactly what failed and suggest how to fix it

## Full Backup to GitHub (4:30 AM daily)
Back up everything that defines how the agent works:
- SOUL.md, MEMORY.md, and all memory/personality files
- All cron job definitions
- All skill configurations
- Gateway config file
- All workspace files and custom workflow definitions
- Any config needed to restore setup from scratch

### Pre-Push Security Scan
1. Scan ALL files for leaked secrets: API keys, tokens, passwords, credentials, private URLs
2. Check environment variables, config files, anything with sensitive data
3. Replace found secrets with descriptive placeholders: [CLAUDE_API_KEY], [DISCORD_BOT_TOKEN], etc.
4. Commit with message including date and summary of changes since last backup
5. Push to private GitHub backup repository

### Reporting
- One-line confirmation to Discord #monitoring when done
- If any file is missing or push fails, report as error

## Tips

Daily auto-update at 4am and encrypted backup to GitHub at 4:30am. Includes secret scanning before push. From velvet-shark's gist.
