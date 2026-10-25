---
title: "Design a Health Check API Endpoint"
slug: design-a-health-check-api-endpoint
stage: Build
category: "API Design"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-health-check-api-endpoint
---
# Design a Health Check API Endpoint

Get a microservice health endpoint design with dependency checks and example healthy and unhealthy JSON responses for orchestration.

## Prompt

I need to create a health check endpoint for my microservice to be used by my container orchestration system (e.g., Kubernetes) to determine if the service is running and healthy.

Your task is to design a health check API endpoint.

**Instructions:**
1.  **Endpoint Design:** Design a simple `GET /health` endpoint.
2.  **Health Status:** The endpoint should return a JSON response indicating the status of the service. The status should be "healthy" if the service is running correctly, and "unhealthy" otherwise.
3.  **Dependency Checks:** The health check should also verify the status of the service's dependencies, such as its database and any external services it communicates with. The response should include the status of each dependency.

**Output Format:**
Provide the output as a Markdown document. First, describe the design of the health check endpoint. Then, provide example JSON responses for a healthy and an unhealthy service.
