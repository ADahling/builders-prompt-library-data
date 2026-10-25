---
title: "Use a Service Mesh for Fine-Grained Canary Releases"
slug: use-a-service-mesh-for-fine-grained-canary-releases
stage: Ship
category: "Deployment & Launch"
grade: B
score: 72
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/use-a-service-mesh-for-fine-grained-canary-releases
---
# Use a Service Mesh for Fine-Grained Canary Releases

Implement header-based traffic routing in a service mesh to execute targeted canary releases for specific user regions or device types.

Variables: service_mesh_name

## Prompt

You are a platform engineer. Use a service mesh (`{{service_mesh_name}}`) to perform a canary release for a microservice, but only for users from a specific geographic region or users on a specific mobile OS.

Instructions:
1. Deploy the canary version of your service.
2. Write a traffic routing rule that inspects incoming request headers (e.g., `User-Agent`, `X-Country-Code`).
3. Route requests that match the criteria to the canary version, while all other requests go to the stable version.
4. This allows for targeted testing of new features with a specific user segment.

## Tips

Demonstrates the advanced traffic shaping capabilities of a service mesh.
