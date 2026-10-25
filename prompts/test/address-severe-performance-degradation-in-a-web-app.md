---
title: "Address Severe Performance Degradation in a Web App"
slug: address-severe-performance-degradation-in-a-web-app
stage: Test
category: "Critical Bugs"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/address-severe-performance-degradation-in-a-web-app
---
# Address Severe Performance Degradation in a Web App

Diagnose and resolve database-driven latency in a Django application by profiling slow queries and implementing scalable indexing strategies.

## Prompt

You are a performance engineer. A high-traffic web application has experienced a severe performance degradation, with page load times increasing by 500%. Your task is to identify the bottleneck and optimize the application.

Context:
- The application is a Python/Django web app behind a load balancer.
- APM tools show that the database queries are the main source of latency.
- The number of users has recently increased significantly.

Provide:
1. A strategy for identifying the most expensive database queries.
2. An example of how to optimize a slow query using indexing and query rewriting.
3. A plan for load testing the application to ensure it can handle future traffic growth.

## Tips

Focuses on performance analysis and optimization skills.
