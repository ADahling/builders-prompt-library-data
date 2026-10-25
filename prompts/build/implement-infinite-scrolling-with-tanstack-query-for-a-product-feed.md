---
title: "Implement Infinite Scrolling with TanStack Query for a Product Feed"
slug: implement-infinite-scrolling-with-tanstack-query-for-a-product-feed
stage: Build
category: "Frontend & Styling"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-infinite-scrolling-with-tanstack-query-for-a-product-feed
---
# Implement Infinite Scrolling with TanStack Query for a Product Feed

Get a TypeScript React product feed with TanStack Query infinite scrolling, cursor pagination, loading and error states, and a Load More fallback.

Variables: platform_name

## Prompt

Our e-commerce platform, {{platform_name}}, needs an infinite scrolling feature for the product feed to improve user experience and performance. We are using React and TanStack Query (formerly React Query) for data fetching.

Your task is to implement an infinite scroll feature using TanStack Query's 'useInfiniteQuery' hook. The API endpoint for fetching products is '/api/products', and it supports pagination via 'cursor' parameter.

The implementation should:
1.  Use the 'useInfiniteQuery' hook to fetch product pages.
2.  The API returns a 'nextCursor' property in its response, which should be used to fetch the next page.
3.  As the user scrolls down, new pages of products should be automatically fetched and appended to the list.
4.  A loading indicator should be displayed at the bottom of the feed while new data is being fetched.
5.  A 'Load More' button should be available as a fallback for users to manually trigger the next page load.
6.  The solution must handle error states gracefully, displaying an error message if a page fails to load.
7.  The code should be written in TypeScript, with proper types for the API response and query functions.

Provide a complete React component that demonstrates this infinite scrolling functionality. Include the TanStack Query setup and the component that renders the product feed.
