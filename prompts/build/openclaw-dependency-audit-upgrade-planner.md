---
title: "OpenClaw: Dependency Audit & Upgrade Planner"
slug: openclaw-dependency-audit-upgrade-planner
stage: Build
category: "OpenClaw"
grade: C
score: 68
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-dependency-audit-upgrade-planner
---
# OpenClaw: Dependency Audit & Upgrade Planner

Audit project dependencies for version gaps, vulnerabilities, and maintenance risks, then get a prioritized upgrade plan and execution checklist.

## Prompt

# Dependency Audit & Upgrade Planner

## Audit Workflow

### Step 1: Inventory
Parse package.json / requirements.txt / Cargo.toml / go.mod and list:
- Package name, current version, latest version
- Semver distance (patch / minor / major behind)
- Last publish date
- Weekly downloads / GitHub stars (health signal)

### Step 2: Risk Assessment
| Risk Factor | Weight | Criteria |
|-------------|--------|----------|
| Major version behind | 30% | 0 = current, 1 = 1 major, 2 = 2+ majors |
| Known vulnerabilities | 25% | CVE count × severity score |
| Maintainer activity | 15% | Last commit >6 months = risk |
| Download trend | 10% | Declining = risk |
| License change | 10% | Permissive→restrictive = risk |
| Breaking changelog | 10% | Number of breaking changes in upgrade path |

### Step 3: Upgrade Plan
Priority tiers:
1. **Critical** — Known CVEs, actively exploited → upgrade immediately
2. **High** — Major version behind, security advisories → upgrade this sprint
3. **Medium** — Minor/patch behind, no security issues → upgrade this quarter
4. **Low** — Cosmetic, dev-only deps → upgrade when convenient

### Step 4: Upgrade Execution Checklist
For each upgrade:
- [ ] Read changelog for breaking changes
- [ ] Check migration guide
- [ ] Update in isolation (one dep at a time)
- [ ] Run full test suite
- [ ] Verify build succeeds
- [ ] Test critical paths manually
- [ ] Update lockfile
- [ ] Document any code changes required

## Tips

Systematic dependency auditing with risk scoring and prioritized upgrade plans. Works with any package manager.
