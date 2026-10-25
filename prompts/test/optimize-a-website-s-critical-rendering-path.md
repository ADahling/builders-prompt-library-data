---
title: "Optimize a Website\u2019s Critical Rendering Path"
slug: optimize-a-website-s-critical-rendering-path
stage: Test
category: "Performance & Code"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-a-website-s-critical-rendering-path
---
# Optimize a Website’s Critical Rendering Path

Get a critical rendering path guide for slow First Contentful Paint, with browser analysis and CSS, JavaScript, and font loading strategies.

Variables: WebsiteURL

## Prompt

Our website, `{{WebsiteURL}}`, has a slow First Contentful Paint (FCP) because of a poorly optimized critical rendering path. I need a detailed guide on how to analyze and optimize the critical rendering path to improve our site’s loading performance.

Act as a web performance expert and provide a comprehensive guide to optimizing the critical rendering path.

Your response should cover the following:
1. **Critical Rendering Path Explained:** A clear explanation of what the critical rendering path is and how it impacts page load time.
2. **Analysis:** How to use browser developer tools to analyze the critical rendering path of a page and identify bottlenecks.
3. **Optimizing CSS:** A set of strategies to optimize the delivery of CSS, such as inlining critical CSS, deferring non-critical CSS, and removing unused CSS.
4. **Optimizing JavaScript:** A guide to optimizing the execution of JavaScript, such as using the `async` and `defer` attributes, and moving scripts to the bottom of the `<body>`.
5. **Optimizing Fonts:** How to optimize the loading of web fonts to avoid blocking the rendering of the page.
