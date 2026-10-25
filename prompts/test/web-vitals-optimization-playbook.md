---
title: "Web Vitals Optimization Playbook"
slug: web-vitals-optimization-playbook
stage: Test
category: "Performance & Code"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/web-vitals-optimization-playbook
---
# Web Vitals Optimization Playbook

Generate a technical roadmap including specific code adjustments to achieve passing Core Web Vitals scores for LCP, INP, and CLS.

Variables: website_url, current_lcp, current_inp, current_cls

## Prompt

You are a Core Web Vitals specialist. Create an optimization playbook to achieve green scores for {{website_url}}.

Current scores:
- LCP: {{current_lcp}}
- INP: {{current_inp}}
- CLS: {{current_cls}}

Target: All metrics in 'Good' range (LCP <2.5s, INP <200ms, CLS <0.1)

**LCP Optimization:**
1. Identify the LCP element
2. Optimize server response time (TTFB)
3. Eliminate render-blocking resources
4. Optimize the LCP resource (preload, compress, resize)
5. Implement priority hints

**INP Optimization:**
1. Identify the slowest interactions
2. Break up long tasks (yield to main thread)
3. Optimize event handlers
4. Reduce JavaScript execution time
5. Use web workers for heavy computation

**CLS Optimization:**
1. Set explicit dimensions on images and videos
2. Reserve space for dynamic content
3. Avoid inserting content above existing content
4. Use CSS containment
5. Optimize web font loading

Provide specific code changes and expected score improvements.

## Tips

Core Web Vitals directly impact Google search ranking. Green scores = better SEO = more traffic.
