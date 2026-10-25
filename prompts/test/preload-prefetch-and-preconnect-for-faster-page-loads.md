---
title: "Preload, Prefetch, and Preconnect for Faster Page Loads"
slug: preload-prefetch-and-preconnect-for-faster-page-loads
stage: Test
category: "Performance & Code"
grade: C
score: 66
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/preload-prefetch-and-preconnect-for-faster-page-loads
---
# Preload, Prefetch, and Preconnect for Faster Page Loads

Get a website resource hints guide explaining when to use preload, prefetch, preconnect, and dns-prefetch, and how to add them to HTML.

## Prompt

I want to improve the loading performance of our website by using resource hints to give the browser clues about what resources will be needed soon. I need a guide on how to use resource hints like `preload`, `prefetch`, and `preconnect`.

Your task is to provide a comprehensive guide to implementing a resource hints strategy.

Your response should include:
1.  **`preload`:** An explanation of what `preload` is and when to use it to fetch a resource that is needed for the current navigation.
2.  **`prefetch`:** A guide to using `prefetch` to fetch a resource that will be needed for a future navigation.
3.  **`preconnect`:** A tutorial on how to use `preconnect` to establish a connection to a third-party domain before a request is made.
4.  **`dns-prefetch`:** A discussion of when to use `dns-prefetch` to speed up DNS lookups for third-party domains.
5.  **Implementation:** How to add resource hints to the `<head>` of your HTML document.
