---
title: "Design a System for Geographically Distributing Data"
slug: design-a-system-for-geographically-distributing-data
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 71
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-system-for-geographically-distributing-data
---
# Design a System for Geographically Distributing Data

Get a data distribution design for a global app, covering regional storage, residency, synchronization, query routing, and consistency.

Variables: current_region

## Prompt

Our application is growing globally, and we need to reduce latency for our users in different parts of the world. To achieve this, I want to design a system for geographically distributing our data. Our primary database is currently located in {{current_region}}.

Your task is to design a system for geographically distributing our data. The design should include:

1.  **Distribution Strategy:** A recommendation for a data distribution strategy. This could involve using a globally distributed database like Google Spanner or Amazon Aurora Global Database, or it could involve setting up read replicas in different regions.
2.  **Data Residency:** A plan for how to handle data residency requirements, such as GDPR, which may require that certain data be stored in a specific region.
3.  **Data Synchronization:** A description of how to keep the data in the different regions in sync. This should include a discussion of the trade-offs between synchronous and asynchronous replication.
4.  **Query Routing:** A design for a system that can route user requests to the nearest data center to reduce latency.
5.  **Consistency Model:** A discussion of the consistency model for the distributed database. This should include an explanation of the trade-offs between strong consistency and eventual consistency.

## Tips

This prompt is for developers who are building global applications and need to design a scalable and low-latency data architecture.
