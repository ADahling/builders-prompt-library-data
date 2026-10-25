---
title: "Design a System for Real-Time Data Replication"
slug: design-a-system-for-real-time-data-replication
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 71
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-system-for-real-time-data-replication
---
# Design a System for Real-Time Data Replication

Get a real-time replication design for remote disaster recovery, with method and topology choices, setup, monitoring, and failover plans.

Variables: database_type

## Prompt

We need to replicate our data in real-time to a remote location for disaster recovery purposes. I need to design a system for real-time data replication for our {{database_type}} database.

Your task is to design a system for real-time data replication. The design should include:

1.  **Replication Method:** A recommendation for a real-time replication method. This could be log-based replication or trigger-based replication. Justify your choice based on our requirements.
2.  **Replication Topology:** A recommendation for a replication topology. This could be a simple master-slave topology or a more complex multi-master topology.
3.  **Replication Setup:** A plan for how to set up the real-time replication. This should include how to configure the master and the slave databases and how to start the replication process.
4.  **Replication Monitoring:** A plan for how to monitor the real-time replication to ensure that it is working as expected. This should include how to check the replication lag and how to detect any replication errors.
5.  **Replication Failover:** A plan for how to failover to the replica database in case of a failure of the primary database.

## Tips

This prompt is for organizations that need to ensure the high availability of their data.
