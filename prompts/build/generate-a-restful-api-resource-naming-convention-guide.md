---
title: "Generate a RESTful API Resource Naming Convention Guide"
slug: generate-a-restful-api-resource-naming-convention-guide
stage: Build
category: "API Design"
grade: A
score: 82
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-restful-api-resource-naming-convention-guide
---
# Generate a RESTful API Resource Naming Convention Guide

Establish a standardized RESTful API naming convention guide defining resource plurality, nested structures, versioning, and case styles for backend teams.

## Prompt

As a senior API architect, I need to establish a clear and consistent resource naming convention for our new e-commerce platform. The platform deals with resources like 'customers', 'products', 'orders', 'reviews', and 'payments'.

Your task is to generate a comprehensive API resource naming convention guide. This guide will be the single source of truth for all developers on the team.

**Instructions:**
1.  **Resource Naming:** Define a clear standard for naming resources. Should we use plural or singular nouns? Provide a definitive answer and justify your choice with examples (e.g., '/products' vs. '/product').
2.  **URI Structure:** Specify the structure for nested resources. For example, how should we represent the relationship between 'customers' and their 'orders'? Show the URI structure for retrieving all orders for a specific customer, and for retrieving a single specific order.
3.  **Versioning:** Recommend a versioning strategy (e.g., URI versioning). Explain how to incorporate the version number into the URI, like '/api/v1/products'.
4.  **Case Convention:** Define the case convention for resource names (e.g., kebab-case, snake_case, camelCase). Choose one and explain why it's a good fit for RESTful APIs.

**Output Format:**
Provide the output as a Markdown document. Use clear headings for each section (Resource Naming, URI Structure, Versioning, Case Convention). Provide at least two positive and two negative examples for each rule to make the guidelines easy to understand.

**Example Snippet (for URI Structure):**
*   **Correct:** '`GET /customers/123/orders`'
*   **Incorrect:** '`GET /customerOrders/123`'
