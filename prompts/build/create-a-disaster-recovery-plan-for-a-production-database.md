---
title: "Create a Disaster Recovery Plan for a Production Database"
slug: create-a-disaster-recovery-plan-for-a-production-database
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 70
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-disaster-recovery-plan-for-a-production-database
---
# Create a Disaster Recovery Plan for a Production Database

Plan production database disaster recovery with RPO and RTO targets, backups, remote replication, failover, failback, and regular testing.

Variables: database_type

## Prompt

Our production database is a critical component of our application, and we need to have a plan in place to recover it in case of a disaster, such as a natural disaster or a major hardware failure. I need to create a disaster recovery plan for our {{database_type}} database.

Your task is to create a disaster recovery plan. The plan should include:

1.  **Recovery Point Objective (RPO) and Recovery Time Objective (RTO):** A definition of our RPO (i.e., how much data we can afford to lose) and our RTO (i.e., how quickly we need to recover the database). These objectives will drive the design of our disaster recovery solution.
2.  **Backup and Replication:** A strategy for backing up our database and for replicating it to a remote location. The replication should be asynchronous to avoid impacting the performance of the production database.
3.  **Failover Process:** A step-by-step process for failing over to the replica database in case of a disaster. The process should be well-documented and should be tested regularly.
4.  **Failback Process:** A step-by-step process for failing back to the primary database after the disaster has been resolved.
5.  **Testing:** A plan for how to test the disaster recovery plan regularly to ensure that it works as expected.

## Tips

This prompt is a critical document for any organization that needs to ensure the high availability of its database.
