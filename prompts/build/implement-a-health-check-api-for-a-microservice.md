---
title: "Implement a Health Check API for a Microservice"
slug: implement-a-health-check-api-for-a-microservice
stage: Build
category: "Backend & Data Integrity"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-a-health-check-api-for-a-microservice
---
# Implement a Health Check API for a Microservice

Get a microservice health check API example for container orchestration, with status responses, dependency checks, and liveness and readiness probes.

Variables: microservice_name, programming_language

## Prompt

I need to implement a health check API for our {{microservice_name}} microservice. The health check API will be used by our container orchestration system (e.g., Kubernetes) to determine if the service is healthy and ready to receive traffic.

Your task is to create a health check API. The implementation should include:

1.  **Health Check Endpoint:** A dedicated endpoint (e.g., `/healthz`) that returns the health status of the service.
2.  **Health Status:** A clear and consistent format for the health status response. The response should indicate whether the service is healthy or not, and it should include details about the status of its dependencies (e.g., the database, other microservices).
3.  **Liveness vs. Readiness:** An explanation of the difference between a liveness probe and a readiness probe, and how to implement both in the health check API.
4.  **Dependency Checks:** A plan for how to check the health of the service's dependencies. This should involve making a lightweight request to each dependency to ensure that it is available and responding correctly.
5.  **Code Example:** A code example in {{programming_language}} that shows how to implement the health check API.

## Tips

This prompt is an essential feature for any microservice that is deployed in a containerized environment.
