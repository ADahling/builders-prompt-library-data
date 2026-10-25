---
title: "Database Backup Verification Playbook"
slug: database-backup-verification-playbook
stage: Build
category: "Backend & Data Integrity"
grade: C
score: 61
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/database-backup-verification-playbook
---
# Database Backup Verification Playbook

Get a database backup audit and monthly restore test playbook, with isolated recovery, integrity checks, app smoke tests, and result tracking.

Variables: timestamp, minutes, percentage, count

## Prompt

# Database Backup Verification Playbook

## Backup Strategy Audit
- [ ] What is backed up? (all tables? storage? auth data?)
- [ ] How often? (continuous WAL / hourly / daily / weekly)
- [ ] Where stored? (same region? cross-region? different provider?)
- [ ] Retention period? (7 days? 30 days? 1 year?)
- [ ] Encrypted at rest?
- [ ] Who has access? (principle of least privilege)

## Backup Types
| Type | RPO | RTO | Use Case |
|------|-----|-----|----------|
| Continuous (WAL/PITR) | ~0 | Minutes | Production databases |
| Daily snapshots | 24h | 1-4 hours | Standard protection |
| Logical dump (pg_dump) | At dump time | Hours | Schema migration safety |
| Cross-region replication | ~0 | Minutes | Disaster recovery |

## Monthly Restore Test Protocol

### Step 1: Restore to Isolated Environment
Never restore to production. Create isolated test database and restore. Record time and errors.

### Step 2: Verify Data Integrity
- Row counts match expected values
- Critical tables have expected record counts
- Referential integrity intact (no orphaned foreign keys)
- Data freshness: latest timestamps within expected window

### Step 3: Application Smoke Test
- [ ] Login works (auth tables restored)
- [ ] Key queries return expected results
- [ ] No missing foreign key references

### Step 4: Document Results
| Metric | Value |
|--------|-------|
| Backup timestamp | {{timestamp}} |
| Restore duration | {{minutes}} |
| Data completeness | {{percentage}} |
| Errors encountered | {{count}} |
| Test passed | ✅ / ❌ |

## Alerting
- [ ] Alert if backup job fails
- [ ] Alert if backup size drops >20%
- [ ] Alert if backup age > 2x expected interval
- [ ] Monthly calendar reminder for restore test

## Tips

Database backup verification playbook with restore testing protocol, integrity checks, and alerting.
