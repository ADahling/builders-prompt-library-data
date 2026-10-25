---
title: "Website Performance Audit and Optimization"
slug: website-performance-audit-and-optimization
stage: Build
category: "Website Cloning"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/website-performance-audit-and-optimization
---
# Website Performance Audit and Optimization

Analyze website speed using audit tools to identify critical bottlenecks and provide a prioritized roadmap for optimizing load times.

Variables: cloned_website_url

## Prompt

You are a web performance analyst. Your task is to audit a cloned website for performance bottlenecks and suggest improvements. The website is image-heavy and has a lot of JavaScript, making it slow to load.

Context:
- The cloned website is located at {{cloned_website_url}}.
- You must use Google PageSpeed Insights and GTmetrix to analyze the website's performance.
- Your report should identify the top 3-5 performance issues and provide actionable recommendations to fix them.

Provide:
1. A performance audit report with scores and metrics from the analysis tools.
2. A prioritized list of recommendations for optimization, including expected impact.

If you cannot open {{cloned_website_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

A practical exercise for learning how to diagnose and fix common web performance problems.
