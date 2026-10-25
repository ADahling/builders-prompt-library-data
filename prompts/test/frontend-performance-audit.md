---
title: "Frontend Performance Audit"
slug: frontend-performance-audit
stage: Test
category: "Quality Audits"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/frontend-performance-audit
---
# Frontend Performance Audit

Optimize application load times and UX by identifying bottlenecks in Core Web Vitals, bundles, and assets with actionable code-level fixes.

Variables: application_url

## Prompt

You are a web performance expert. Conduct a comprehensive frontend performance audit for {{application_url}}.

Audit areas:
1. **Core Web Vitals**: LCP, FID/INP, CLS - measure and optimize each
2. **Bundle Analysis**: JavaScript bundle size, tree-shaking effectiveness, code splitting
3. **Image Optimization**: Format (WebP/AVIF), sizing, lazy loading, responsive images
4. **Font Loading**: Font display strategy, subsetting, preloading
5. **Caching Strategy**: Service worker, HTTP cache headers, CDN configuration
6. **Critical Rendering Path**: Render-blocking resources, above-the-fold optimization
7. **Third-Party Scripts**: Impact assessment, loading strategy (async/defer/facade)
8. **Network Optimization**: HTTP/2, compression, prefetching, preconnecting

For each finding:
- Current metric value
- Target metric value
- Specific fix with code example
- Expected improvement

Prioritize fixes by impact-to-effort ratio.

## Tips

Performance directly impacts SEO ranking and conversion rates. A 1-second delay reduces conversions by 7%.
