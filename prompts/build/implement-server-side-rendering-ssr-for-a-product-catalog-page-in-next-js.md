---
title: "Implement Server-Side Rendering (SSR) for a Product Catalog Page in Next.js"
slug: implement-server-side-rendering-ssr-for-a-product-catalog-page-in-next-js
stage: Build
category: "Frontend & Styling"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-server-side-rendering-ssr-for-a-product-catalog-page-in-next-js
---
# Implement Server-Side Rendering (SSR) for a Product Catalog Page in Next.js

Get a TypeScript Next.js product catalog page using getServerSideProps, with API error handling, typed product data, and a mock response.

Variables: website_name

## Prompt

To improve SEO and the initial page load performance of our e-commerce site, {{website_name}}, we need to implement Server-Side Rendering (SSR) for our product catalog page. The page displays a list of products fetched from an external API.

Create a Next.js page component that uses SSR to fetch and render a list of products. The page should be located at 'pages/products/index.tsx' (assuming the Pages Router for this SSR task).

The implementation must:
1.  Use the 'getServerSideProps' function to fetch the product data from an API endpoint (e.g., 'https://api.example.com/products') on each request.
2.  The fetched data should be passed as props to the page component.
3.  The page component should then render the list of products, displaying their name, price, and image.
4.  The data fetching in 'getServerSideProps' must be resilient to API errors. If the fetch fails, it should handle the error gracefully, perhaps by passing an empty list of products or an error prop to the component.
5.  The code must be written in TypeScript, with proper types for the props and the product data.

Provide the complete code for the 'pages/products/index.tsx' file. Include a mock of the API response for context. The comments should explain how 'getServerSideProps' works and why it's beneficial for this use case.
