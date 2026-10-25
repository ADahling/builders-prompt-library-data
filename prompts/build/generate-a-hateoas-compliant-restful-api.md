---
title: "Generate a HATEOAS-compliant RESTful API"
slug: generate-a-hateoas-compliant-restful-api
stage: Build
category: "API Design"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-hateoas-compliant-restful-api
---
# Generate a HATEOAS-compliant RESTful API

Design a product API with a HATEOAS explanation, hypermedia format choice, and JSON responses with links for listing and viewing products.

## Prompt

I want to design a truly RESTful API that follows the HATEOAS (Hypermedia as the Engine of Application State) constraint. This will allow clients to dynamically navigate the API by following links in the responses.

Your task is to design a HATEOAS-compliant API for a simple resource, for example, a "product" in an e-commerce application.

**Instructions:**
1.  **HATEOAS Explained:** Briefly explain the concept of HATEOAS and its benefits.
2.  **Hypermedia Format:** Choose a hypermedia format for your API (e.g., HAL, JSON:API, Siren) and explain why you chose it.
3.  **API Design:** Design the responses for the following requests to a `/products` endpoint:
    *   `GET /products` (list of products)
    *   `GET /products/{id}` (single product)
    The responses should include hypermedia controls (links) that allow the client to perform actions like navigating to the next page of products, viewing a single product, or adding a product to the cart.

**Output Format:**
Provide the output as a Markdown document. Start with an explanation of HATEOAS. Then, for each of the two requests, provide the full JSON response including the hypermedia links, using the format you have chosen.
