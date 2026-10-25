---
title: "Implement Dynamic Routing and Data Fetching in Next.js with the App Router"
slug: implement-dynamic-routing-and-data-fetching-in-next-js-with-the-app-router
stage: Build
category: "Frontend & Styling"
grade: A
score: 89
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-dynamic-routing-and-data-fetching-in-next-js-with-the-app-router
---
# Implement Dynamic Routing and Data Fetching in Next.js with the App Router

Get a Next.js App Router blog page with dynamic slugs, mock server-side fetching, static generation, post rendering, and error and 404 handling.

Variables: blog_name

## Prompt

Our blog, {{blog_name}}, is being built with Next.js and the App Router. We need to create dynamic routes for individual blog posts. Each post should have its own page, and the data for the post should be fetched on the server.

Your task is to implement a dynamic route for blog posts, where the URL structure is '/blog/[slug]'. The data for each post is fetched from a headless CMS via a REST API.

The implementation must:
1.  Create a dynamic route segment at 'app/blog/[slug]/page.tsx'.
2.  Use server-side data fetching within the page component to get the post data based on the 'slug' parameter.
3.  Implement 'generateStaticParams' to pre-build the static pages for all blog posts at build time (SSG), improving performance and SEO.
4.  The page should display the post's title, content, and author.
5.  Handle the case where a post with the given slug is not found by showing a 404 page.
6.  The data fetching function should be robust and include error handling.

Provide the complete code for the 'app/blog/[slug]/page.tsx' file. Include a mock data-fetching function to simulate calling the headless CMS API. The code should be well-commented to explain the role of dynamic segments, data fetching, and 'generateStaticParams'.
