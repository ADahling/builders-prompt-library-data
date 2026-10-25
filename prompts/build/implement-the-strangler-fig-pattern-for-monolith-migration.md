---
title: "Implement the Strangler Fig Pattern for Monolith Migration"
slug: implement-the-strangler-fig-pattern-for-monolith-migration
stage: Build
category: "System Architecture"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-the-strangler-fig-pattern-for-monolith-migration
---
# Implement the Strangler Fig Pattern for Monolith Migration

Generate a comprehensive technical migration plan to decompose a monolithic feature into a microservice using the Strangler Fig pattern.

Variables: app_type, app_name, tech_stack, feature_to_extract

## Prompt

You are a senior software engineer tasked with leading the migration of a legacy monolithic application to a microservices architecture. Your team has decided to use the Strangler Fig pattern to minimize risk and ensure a gradual, controlled transition.

**Application Context:**
The monolith is a {{app_type}} application named '{{app_name}}' built with {{tech_stack}}. We want to start by strangling the '{{feature_to_extract}}' functionality and replacing it with a new microservice.

**Your Task:**
Create a detailed technical plan for implementing the Strangler Fig pattern for this specific feature. The plan should provide code examples and clear instructions for the development team.

**Instructions & Constraints:**
1.  **Proxy/Facade Layer:**
    *   Design a proxy layer that will sit in front of the monolith. This proxy will intercept incoming requests for the '{{feature_to_extract}}' and route them to the new microservice. All other requests should be passed through to the monolith.
    *   Provide code examples for setting up this proxy using a tool like Nginx, HAProxy, or an API Gateway (e.g., Kong, AWS API Gateway).

2.  **New Microservice Development:**
    *   Outline the steps for developing the new '{{feature_to_extract}}' microservice.
    *   Specify the API contract for the new service, ensuring it's compatible with the existing functionality.

3.  **Data Migration and Synchronization:**
    *   Describe the strategy for migrating the data related to '{{feature_to_extract}}' from the monolith's database to the new microservice's database.
    *   Explain how to keep the data synchronized between the two systems during the transition period.

4.  **Testing and Rollout:**
    *   Detail the testing strategy to ensure the new microservice works as expected and that the integration with the monolith is seamless.
    *   Propose a gradual rollout plan (e.g., canary release, blue-green deployment) to minimize the impact of any potential issues.

5.  **Monitoring and Logging:**
    *   Specify the key metrics to monitor for both the new microservice and the proxy layer.
    *   Describe the logging strategy to help debug issues during and after the migration.

**Output Format:**
Generate a Markdown document with the following sections:
1.  **Overview of the Strangler Fig Implementation**
2.  **Proxy Layer Configuration (with code examples)**
3.  **New Microservice Development Guide**
4.  **Data Migration and Synchronization Plan**
5.  **Testing and Rollout Strategy**
6.  **Monitoring and Logging Plan**
