---
title: "Implement a Next.js App Router Route Handler for a RESTful API Endpoint"
slug: implement-a-next-js-app-router-route-handler-for-a-restful-api-endpoint
stage: Build
category: "Frontend & Styling"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-a-next-js-app-router-route-handler-for-a-restful-api-endpoint
---
# Implement a Next.js App Router Route Handler for a RESTful API Endpoint

Get a TypeScript Next.js App Router GET handler for PostgreSQL products using Prisma, with pagination, category filtering, and error handling.

## Prompt

Our team is building a new application using Next.js 13+ with the App Router. We need to create a set of RESTful API endpoints to handle CRUD operations for our 'products' resource. The data is stored in a PostgreSQL database, and we are using Prisma as our ORM.

Your task is to implement a route handler for the GET method to fetch a list of products. The endpoint should be located at /api/products. The handler needs to support pagination and filtering by category.

The route handler must:
1.  Be defined within the app/api/products/route.ts file.
2.  Use Prisma Client to query the database for products.
3.  Implement pagination using query parameters: 'page' (page number) and 'limit' (items per page).
4.  Allow filtering products by a 'categoryId' query parameter.
5.  Handle potential errors gracefully, such as database connection issues or invalid query parameters, and return appropriate HTTP status codes (e.g., 500 for server errors, 400 for bad requests).
6.  Return the list of products in JSON format with a 200 OK status on success.
7.  The code must be written in TypeScript.

Provide the full implementation of the app/api/products/route.ts file. Include comments explaining the logic for pagination, filtering, and error handling.
