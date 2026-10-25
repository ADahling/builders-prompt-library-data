---
title: "Fix Insecure `target='_blank'` Links"
slug: fix-insecure-target-blank-links
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 74
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-insecure-target-blank-links
---
# Fix Insecure `target='_blank'` Links

Get a junior-friendly explanation of tabnabbing, link attribute fixes, and an ESLint check for security warnings on new-tab links.

## Prompt

I have a number of external links on my website that use `target="_blank"` to open in a new tab. My linter is giving me a security warning about them, but I don't understand the risk.

Your task is to explain the risk and show me how to fix it.

1.  **The Vulnerability Explained:** In simple terms, explain the "tabnabbing" vulnerability. How can a malicious page that is opened via `target="_blank"` gain partial control over the original page (`window.opener`)?
2.  **The Fix:** Show the simple fix. Explain that I need to add `rel="noopener noreferrer"` to all of my `target="_blank"` links.
3.  **What `noopener` and `noreferrer` Do:** Briefly explain what each of these `rel` attributes does.
    *   `noopener`: Prevents the new page from being able to access the `window.opener` property.
    *   `noreferrer`: Prevents the browser from sending the `Referer` header to the new page.
4.  **Automated Check:** Show how to configure an ESLint rule (e.g., in `eslint-plugin-react`) to automatically catch this issue in the future.

Output should be a simple, clear explanation for a junior developer.

## Tips

A very common and easy-to-fix web security vulnerability.
