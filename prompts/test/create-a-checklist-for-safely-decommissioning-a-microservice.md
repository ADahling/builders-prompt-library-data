---
title: "Create a Checklist for Safely Decommissioning a Microservice"
slug: create-a-checklist-for-safely-decommissioning-a-microservice
stage: Test
category: "Cleanup & Warnings"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-checklist-for-safely-decommissioning-a-microservice
---
# Create a Checklist for Safely Decommissioning a Microservice

Get a phased checklist for retiring a microservice, covering dependencies, consumer rerouting, data migration, shutdown, and cleanup.

Variables: service_name, language

## Prompt

My organization is moving away from a microservices architecture for a particular feature, and we need to decommission the `{{service_name}}` microservice. This service is written in `{{language}}` and has its own database and CI/CD pipeline.

Decommissioning a service is not as simple as just turning it off. It can have unexpected downstream consequences. I need a comprehensive checklist to ensure we do this safely and completely.

Your task is to create this checklist.

The checklist should be organized into phases and cover all aspects of the decommissioning process:

1.  **Phase 1: Analysis & Planning**
    *   Identify all upstream consumers of the service.
    *   Identify all downstream dependencies (databases, other APIs, etc.).
    *   Create a communication plan to notify the owners of the consuming services.
    *   Define a rollback plan in case something goes wrong.
2.  **Phase 2: Rerouting & Migration**
    *   Update all upstream consumers to stop calling the service. (This is the main part of the work).
    *   Migrate any necessary data from the service's database to another database.
3.  **Phase 3: Decommissioning**
    *   Turn off the service in a pre-production environment first and run regression tests.
    *   Take a final backup of the database.
    *   Turn off the production instances of the service.
    *   Update the API gateway or service discovery to remove the service's endpoint.
4.  **Phase 4: Cleanup**
    *   Delete the CI/CD pipeline.
    *   Delete the monitoring dashboards and alerts.
    *   Drop the database.
    *   Archive the source code repository.
    *   Remove the DNS records.
    *   Delete the cloud resources (servers, load balancers, etc.).

Output should be a detailed checklist that can be used as a formal process document.

## Tips

Decommissioning services is a surprisingly complex process that is often overlooked. A formal checklist is essential to avoid leaving behind zombie infrastructure and security holes.
