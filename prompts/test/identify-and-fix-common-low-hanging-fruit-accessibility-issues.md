---
title: "Identify and Fix Common, Low-Hanging-Fruit Accessibility Issues"
slug: identify-and-fix-common-low-hanging-fruit-accessibility-issues
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/identify-and-fix-common-low-hanging-fruit-accessibility-issues
---
# Identify and Fix Common, Low-Hanging-Fruit Accessibility Issues

Audit and resolve foundational web accessibility errors using automated tools and specific HTML code corrections for images, links, and forms.

## Prompt

I am new to web accessibility (a11y), and I want to find and fix some of the most common and easy-to-fix issues on my website to improve it for users with disabilities.

Your task is to provide a checklist of "low-hanging fruit" accessibility issues and show how to fix them.

1.  **Tool Recommendation:** Introduce a browser extension like `axe DevTools` that can automatically scan a page and identify accessibility problems.
2.  **The Checklist:** For each of the following common issues, explain the problem and provide a simple "bad" (inaccessible) and "good" (accessible) HTML code example.
    *   **Images without `alt` text:** `<img>` tags must have an `alt` attribute that describes the image.
    *   **Links without descriptive text:** Link text should make sense out of context (e.g., "Read more about our services" instead of just "Click here").
    *   **Missing form labels:** Every `<input>` should have a corresponding `<label>`.
    *   **Low contrast text:** Text color should have sufficient contrast with its background color.
    *   **Missing document language:** The `<html>` tag should have a `lang` attribute (e.g., `<html lang="en">`).

Output should be a simple, actionable guide for an accessibility beginner.

## Tips

This prompt provides a great starting point for any developer looking to improve the accessibility of their work.
