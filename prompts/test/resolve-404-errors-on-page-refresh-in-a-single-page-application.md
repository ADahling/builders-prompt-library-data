---
title: "Resolve 404 Errors on Page Refresh in a Single Page Application"
slug: resolve-404-errors-on-page-refresh-in-a-single-page-application
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-404-errors-on-page-refresh-in-a-single-page-application
---
# Resolve 404 Errors on Page Refresh in a Single Page Application

Configure web servers to prevent 404 errors on SPA refreshes by implementing rewrite rules that redirect client-side routes to index.html.

Variables: tech_stack, hosting_provider, routing_library

## Prompt

You are a DevOps engineer deploying a Single Page Application (SPA) built with {{tech_stack}} to a {{hosting_provider}} server (e.g., Nginx, Apache, Vercel). The application works perfectly when navigating internally using {{routing_library}}. However, if a user is on a specific route like `/users/123` and refreshes the page, they get a "404 Not Found" error from the server.

Your task is to diagnose this common SPA deployment issue and provide the correct server configuration to fix it.

**Context:**
- **Problem:** The web server doesn't know how to handle client-side routes on a direct request.
- **Goal:** Configure the server to redirect all requests for non-existent files to the `index.html` file, allowing the client-side router to take over.

**Instructions:**

1.  **Explain the Root Cause:** Describe why a web server returns a 404 error for client-side routes in an SPA when the page is refreshed. Explain the difference between server-side routing and client-side routing.
2.  **Provide Server Configuration:** Based on the specified {{hosting_provider}}, provide the necessary configuration file or rules to handle this scenario. For Nginx, this would be a `location` block in the server configuration. For Apache, it would be rules in an `.htaccess` file. For a platform like Vercel or Netlify, it would be a `rewrites` rule in their configuration JSON file.
3.  **Explain the Configuration:** Briefly explain how the provided configuration works to solve the problem. Describe how it serves the `index.html` for any route that doesn't match a static file on the server.

**Output Format:**

- **Root Cause Analysis:** A clear explanation of the SPA routing problem.
- **Server Configuration Snippet:** The configuration code for the specified {{hosting_provider}}.
- **Explanation of the Fix:** A summary of how the server configuration resolves the 404 errors.

## Tips

A classic and essential piece of knowledge for anyone deploying a modern SPA.
