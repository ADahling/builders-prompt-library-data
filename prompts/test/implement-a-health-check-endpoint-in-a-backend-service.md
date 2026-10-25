---
title: "Implement a Health Check Endpoint in a Backend Service"
slug: implement-a-health-check-endpoint-in-a-backend-service
stage: Test
category: "Cleanup & Warnings"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-a-health-check-endpoint-in-a-backend-service
---
# Implement a Health Check Endpoint in a Backend Service

Get a health check endpoint guide and controller code for a containerized backend, covering probes, dependency checks, HTTP statuses, and JSON output.

Variables: language, framework, orchestration_tool

## Prompt

I have a backend service written in `{{language}}` and `{{framework}}`. I am running it in a containerized environment managed by `{{orchestration_tool}}` (e.g., Kubernetes, Docker Swarm). The orchestration tool needs a way to know if my service is healthy and ready to receive traffic.

I need to implement a health check endpoint.

Your task is to provide a guide on how to design and implement a robust health check endpoint.

1.  **Types of Health Checks:** Explain the difference between a "liveness" probe and a "readiness" probe.
    *   **Liveness:** Is the service running? (A simple `200 OK` is often enough).
    *   **Readiness:** Is the service ready to accept traffic? (This might involve checking its dependencies, like a database connection).
2.  **Implementation:** Provide the code for a health check controller in `{{framework}}`. It should expose an endpoint like `/healthz`.
    *   The endpoint should return a `200 OK` status if the service is healthy.
    *   It should return a `503 Service Unavailable` status if it is not healthy.
    *   The response body should be a JSON object containing details about the status of the service and its dependencies (e.g., `{"status": "unhealthy", "dependencies": {"database": "down"}}`).
3.  **Checking Dependencies:** Show how to check the status of critical dependencies, such as a database connection or another API, as part of the health check. This check should have a short timeout to avoid blocking the health check itself.
4.  **Orchestrator Configuration:** Show a snippet of configuration for `{{orchestration_tool}}` (e.g., a Kubernetes deployment YAML) that configures the liveness and readiness probes to use the new health check endpoint.

Output should be a complete guide to this essential operational feature.

## Tips

Health check endpoints are a critical part of building reliable, self-healing systems in a containerized world.
