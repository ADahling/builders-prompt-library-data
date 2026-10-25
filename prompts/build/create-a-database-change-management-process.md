---
title: "Create a Database Change Management Process"
slug: create-a-database-change-management-process
stage: Build
category: "Backend & Data Integrity"
grade: C
score: 66
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-database-change-management-process
---
# Create a Database Change Management Process

Plan a shared database schema change process with request forms, approvals, versioned migration scripts, tooling, and team communication.

## Prompt

In our team, we have multiple developers making changes to the database schema, and it's becoming difficult to keep track of the changes and to ensure that they are applied consistently across all our environments. I want to create a database change management process to bring some order to this chaos.

Your task is to create a database change management process. The process should include:

1.  **Change Request Form:** A template for a change request form that developers must fill out when they want to make a change to the database schema. The form should include a description of the change, the reason for the change, and the potential impact of the change.
2.  **Review and Approval Process:** A process for reviewing and approving the change requests. This should involve getting sign-off from the database administrator, the lead developer, and any other relevant stakeholders.
3.  **Migration Scripts:** A requirement that all database changes be made through migration scripts that are checked into version control. The scripts should be written in a way that they can be run automatically as part of the deployment process.
4.  **Tooling:** A recommendation for a database migration tool (e.g., Flyway, Liquibase) to manage and apply the migration scripts.
5.  **Communication Plan:** A plan for how to communicate database changes to the rest of the team.

## Tips

This prompt is a foundational process for any team that wants to manage its database schema in a controlled and professional way.
