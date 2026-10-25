---
title: "Find and Fix 'Mixed Content' Warnings on an HTTPS Website"
slug: find-and-fix-mixed-content-warnings-on-an-https-website
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/find-and-fix-mixed-content-warnings-on-an-https-website
---
# Find and Fix 'Mixed Content' Warnings on an HTTPS Website

Get a simple guide to HTTPS mixed content warnings, including browser checks, resource URL fixes, and a security policy for prevention.

Variables: page_url

## Prompt

My website is served over HTTPS, but my browser's developer console is showing "mixed content" warnings. It says that the page at `{{page_url}}` was loaded over HTTPS, but requested an insecure resource like an image or a script.

I need to fix this to make my site fully secure and get the green padlock icon in the browser address bar.

Your task is to explain what mixed content is and provide a simple guide to finding and fixing it.

1.  **What is Mixed Content?** Explain what it is and why it's a security risk. Explain the difference between "active" mixed content (like scripts) and "passive" mixed content (like images).
2.  **Finding Mixed Content:** How can I find all the insecure resources being loaded on my page? Show how to use the browser's developer tools (the Network or Console panel) to identify the URLs that are causing the warnings.
3.  **Fixing the Problem:** What is the fix? Explain that the solution is to change the URL of the insecure resource from `http://` to `https://`. What if the resource is not available over HTTPS?
4.  **Prevention:** How can I prevent this from happening in the future? Introduce the `Content-Security-Policy` `upgrade-insecure-requests` directive as an automated way to prevent mixed content issues.

Output should be a simple, non-technical guide to fixing this common web security issue.

## Tips

A very common issue when migrating a website to HTTPS. This prompt provides a clear and simple solution.
