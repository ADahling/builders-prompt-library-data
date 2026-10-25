---
title: "Generate a Plan for Upgrading a Production Database"
slug: generate-a-plan-for-upgrading-a-production-database
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-plan-for-upgrading-a-production-database
---
# Generate a Plan for Upgrading a Production Database

Plan a production database version upgrade with preparation checklists, staging tests, upgrade commands, rollback steps, and post-upgrade checks.

Variables: database_type, current_version, new_version

## Prompt

We are planning to upgrade our production {{database_type}} database from version {{current_version}} to version {{new_version}}. This is a major upgrade with many new features and potential breaking changes. I need a comprehensive plan to ensure that the upgrade is smooth and successful, with minimal downtime.

Your task is to generate a detailed database upgrade plan. The plan should include:

1.  **Pre-Upgrade Checklist:** A checklist of all the tasks that need to be performed before the upgrade. This should include reading the release notes, checking for deprecated features, and backing up the database.
2.  **Testing Strategy:** A strategy for testing the new database version in a staging environment. This should involve running our application's test suite and performing manual testing to identify any compatibility issues.
3.  **Upgrade Procedure:** A step-by-step procedure for performing the upgrade. This should include the commands to run and the expected output. The procedure should be designed to minimize downtime.
4.  **Rollback Plan:** A detailed rollback plan in case the upgrade fails or causes critical issues. The rollback plan should specify how to restore the database to its original state.
5.  **Post-Upgrade Checklist:** A checklist of all the tasks that need to be performed after the upgrade. This should include updating database statistics, monitoring the database for any issues, and communicating the successful upgrade to the team.

## Tips

This prompt is a critical task for any database administrator or developer who is responsible for maintaining a production database.
