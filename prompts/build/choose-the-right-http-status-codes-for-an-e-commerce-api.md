---
title: "Choose the Right HTTP Status Codes for an E-commerce API"
slug: choose-the-right-http-status-codes-for-an-e-commerce-api
stage: Build
category: "API Design"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/choose-the-right-http-status-codes-for-an-e-commerce-api
---
# Choose the Right HTTP Status Codes for an E-commerce API

Map appropriate HTTP status codes to common e-commerce API scenarios to ensure consistent error handling and RESTful communication.

## Prompt

As a junior developer building an e-commerce API, I need help understanding and choosing the correct HTTP status codes for various scenarios. Please act as a senior engineer and provide a detailed guide.

**Scenarios to cover:**

1.  Successfully retrieving a product.
2.  Creating a new customer account.
3.  A user trying to access an order that doesn't belong to them.
4.  A request to update a product with invalid data (e.g., a negative price).
5.  A user who is not authenticated trying to access their shopping cart.
6.  Successfully deleting a product from the catalog.
7.  A request to a deprecated API endpoint.
8.  The server encountering an unexpected error while processing a payment.

**Instructions:**
For each scenario, explain which HTTP status code is most appropriate and why. Describe what the client should do upon receiving that status code. Also, provide a brief overview of the different classes of HTTP status codes (1xx, 2xx, 3xx, 4xx, 5xx) and their general meaning.

**Output Format:**
Use a Markdown table with columns for "Scenario", "HTTP Status Code", "Reasoning", and "Client Action".
