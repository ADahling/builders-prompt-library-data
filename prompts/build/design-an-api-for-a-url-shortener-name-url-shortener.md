---
title: "Design an API for a URL Shortener"
slug: design-an-api-for-a-url-shortener-name-url-shortener
stage: Build
category: "API Design"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-an-api-for-a-url-shortener-name-url-shortener
---
# Design an API for a URL Shortener

Get a URL shortener API design with methods, URIs, and request/response formats for short link creation, custom aliases, and click analytics.

Variables: url_shortener_name

## Prompt

I am building a URL shortener service called {{url_shortener_name}}, similar to Bitly or TinyURL. I need to design the API for it.

Your task is to design the core API for the URL shortener.

**Instructions:**
1.  **Core Functionality:** Design the API endpoint for creating a short URL from a long URL.
2.  **Analytics:** Design the API endpoint for retrieving analytics for a short URL (e.g., number of clicks, referrers, locations).
3.  **Customization:** Design the API endpoint for creating custom short URLs (e.g., with a custom alias).

**Output Format:**
Provide the output as a Markdown document. For each feature, describe the design of the corresponding API endpoint, including the HTTP method, URI, and request/response format.
