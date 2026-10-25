---
title: "Implementing an API for Product Inventory"
slug: implementing-an-api-for-product-inventory
stage: Build
category: "API Design"
grade: B
score: 73
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-an-api-for-product-inventory
---
# Implementing an API for Product Inventory

Design a RESTful inventory API for listing, filtering, adding, updating, and removing products, with response formats and error handling.

Variables: category, name, quantity, price

## Prompt

Design a RESTful API for managing product inventory. Include endpoints for:
- {GET /inventory}: Retrieving a list of products with optional filtering by {{category}}.
- {POST /inventory}: Adding new products with fields {{name}}, {{quantity}}, and {{price}}.
- {PUT /inventory/{productId}}: Updating product details by {productId}.
- {DELETE /inventory/{productId}}: Removing a product from inventory. Discuss response formats and error handling.

## Tips

This prompt will help you manage inventory effectively in your application.
