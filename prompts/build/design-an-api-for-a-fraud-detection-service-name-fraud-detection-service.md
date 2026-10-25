---
title: "Design an API for a Fraud Detection Service"
slug: design-an-api-for-a-fraud-detection-service-name-fraud-detection-service
stage: Build
category: "API Design"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-fraud-detection-service-name-fraud-detection-service
---
# Design an API for a Fraud Detection Service

Get a fraud scoring endpoint design for transactions or events, plus real-time versus batch detection trade-offs and their impact on the API.

Variables: fraud_detection_service_name

## Prompt

I am building a fraud detection service called {{fraud_detection_service_name}}. I need to design the API for it.

Your task is to design the core API for the service.

**Instructions:**
1.  **Fraud Detection Endpoint:** Design an API endpoint that takes a transaction or an event as input and returns a fraud score or a risk assessment.
2.  **Real-time vs. Batch:** Discuss the trade-offs between real-time and batch fraud detection and how this would affect your API design.

**Output Format:**
Provide the output as a Markdown document. Describe the design of the fraud detection endpoint and discuss the real-time vs. batch considerations.
