---
title: "Optimize the Performance of a Third-Party Script"
slug: optimize-the-performance-of-a-third-party-script-2
stage: Test
category: "Performance & Code"
grade: A+
score: 92
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-the-performance-of-a-third-party-script-2
---
# Optimize the Performance of a Third-Party Script

Get a guide for third-party scripts slowing your site, covering impact analysis, deferred and lazy loading, local hosting, and sandboxing.

Variables: WebsiteURL, ScriptName

## Prompt

Our website, `{{WebsiteURL}}`, uses a third-party script, `{{ScriptName}}`, for analytics/ads/etc., and it is slowing down our site. I need a set of strategies to reduce the performance impact of this third-party script.

Act as a web performance expert and provide a detailed guide to optimizing the performance of a third-party script.

Your response should cover the following:
1. **Performance Impact Analysis:** How to analyze the performance impact of a third-party script using tools like WebPageTest and Lighthouse.
2. **Asynchronous and Deferred Loading:** A guide to loading the third-party script asynchronously or deferring its execution to avoid blocking the rendering of the page.
3. **Hosting the Script Locally:** A discussion of the pros and cons of hosting the third-party script on your own server versus loading it from the vendor's CDN.
4. **Lazy Loading:** How to lazy-load the third-party script only when it is needed, for example, when the user scrolls to a certain part of the page.
5. **Sandboxing:** How to use sandboxing techniques to isolate the third-party script and limit its ability to impact the performance of your site.
