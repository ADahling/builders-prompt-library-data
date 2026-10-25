---
title: "Core Web Vitals Monitoring and Optimization"
slug: core-web-vitals-monitoring-and-optimization
stage: Ship
category: "Monitoring & Observability"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/core-web-vitals-monitoring-and-optimization
---
# Core Web Vitals Monitoring and Optimization

Get a Core Web Vitals monitoring plan for your site, with thresholds, a weekly reporting script, and optimization guidance for failing metrics.

Variables: monitoring_tool, website_url

## Prompt

Using the {{monitoring_tool}}, create a monitoring plan to track Core Web Vitals for {{website_url}}. Your task is to collect metrics such as Largest Contentful Paint (LCP), First Input Delay (FID), and Cumulative Layout Shift (CLS). Set thresholds that align with Google's recommendations for these metrics. Develop a script that automatically generates a weekly report summarizing the collected data and any violations of the set thresholds. Propose optimizations to improve any metrics that do not meet the required standards. Provide a detailed explanation of the steps taken and any code changes needed to implement these optimizations.

## Tips

This prompt is suitable for developers familiar with Core Web Vitals and performance optimization techniques.
