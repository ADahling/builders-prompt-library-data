---
title: "OpenClaw: Frontend Performance Budget"
slug: openclaw-frontend-performance-budget
stage: Build
category: "OpenClaw"
grade: C
score: 60
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-frontend-performance-budget
---
# OpenClaw: Frontend Performance Budget

Get frontend performance budgets, CI enforcement settings, and an optimization checklist for page speed, asset sizes, and requests.

## Prompt

# Frontend Performance Budget

## Budget Targets

### Core Web Vitals (2025 thresholds)
| Metric | Good | Needs Improvement | Poor |
|--------|------|-------------------|------|
| LCP (Largest Contentful Paint) | ≤ 2.5s | ≤ 4.0s | > 4.0s |
| INP (Interaction to Next Paint) | ≤ 200ms | ≤ 500ms | > 500ms |
| CLS (Cumulative Layout Shift) | ≤ 0.1 | ≤ 0.25 | > 0.25 |
| TTFB (Time to First Byte) | ≤ 800ms | ≤ 1800ms | > 1800ms |

### Size Budgets
| Resource | Budget | Measurement |
|----------|--------|-------------|
| Total page weight | ≤ 500KB | Compressed (gzip/brotli) |
| JavaScript | ≤ 200KB | Compressed, initial load |
| CSS | ≤ 50KB | Compressed, initial load |
| Images (above fold) | ≤ 200KB | Optimized (WebP/AVIF) |
| Web fonts | ≤ 100KB | WOFF2, subset |
| Third-party scripts | ≤ 50KB | Total, all vendors |

### Request Budgets
| Metric | Budget |
|--------|--------|
| HTTP requests (initial) | ≤ 25 |
| Third-party domains | ≤ 5 |
| Blocking resources | 0 (all async/defer) |

## Enforcement

### CI Pipeline Checks
```yaml
performance_budget:
  lighthouse:
    performance: 90
    accessibility: 95
    best_practices: 95
    seo: 95
  bundle_size:
    main: 150KB
    vendor: 100KB
    total: 300KB
    fail_on_exceed: true
  web_vitals:
    lcp: 2500
    inp: 200
    cls: 0.1
```

### Optimization Checklist
- [ ] Code splitting: route-based + component-based lazy loading
- [ ] Tree shaking: no barrel file re-exports of large libraries
- [ ] Image optimization: WebP/AVIF, responsive srcset, lazy loading
- [ ] Font optimization: subset, font-display: swap, preload critical
- [ ] Preload/prefetch: critical path resources
- [ ] Service worker: cache-first for static, network-first for API
- [ ] Bundle analysis: run on every PR, visualize with source-map-explorer
- [ ] Third-party audit: load non-critical scripts after onload

## Tips

Frontend performance budget with Core Web Vitals targets, size/request budgets, CI enforcement configuration, and optimization checklist.
