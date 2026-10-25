---
title: "Clone SEO & Performance Configuration"
slug: clone-seo-performance-configuration
stage: Build
category: "Website Cloning"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-seo-performance-configuration
---
# Clone SEO & Performance Configuration

Reverse-engineer a target website's SEO architecture and performance stack to generate production-ready configurations and optimization code.

Variables: target_url

## Prompt

You are an SEO and web performance engineer. Analyze the target website and reproduce its complete SEO and performance optimization setup.

Target URL: {{target_url}}

## SEO Reproduction
1. **Meta Tags**: Title template, description, Open Graph (og:title, og:description, og:image, og:type), Twitter Card tags.
2. **Structured Data**: JSON-LD schemas (Organization, WebSite, BreadcrumbList, Product, FAQ, Article).
3. **Sitemap**: Generate sitemap.xml with all routes, priorities, and change frequencies.
4. **Robots.txt**: Crawl directives, sitemap reference, disallow patterns.
5. **Canonical URLs**: Strategy for duplicate content prevention.
6. **Internal Linking**: Navigation structure optimized for crawl depth.

## Performance Reproduction
1. **Image Optimization**: Format (WebP/AVIF), sizing strategy, lazy loading, blur placeholder.
2. **Font Loading**: Font display strategy, preload critical fonts, subset if possible.
3. **Code Splitting**: Route-based lazy loading, dynamic imports for heavy components.
4. **Caching**: Cache-Control headers, service worker strategy, CDN configuration.
5. **Core Web Vitals Targets**: LCP < 2.5s, FID < 100ms, CLS < 0.1 — specific optimizations for each.
6. **Bundle Optimization**: Tree shaking, minification, compression (Brotli/gzip).

## Analytics & Tracking
1. **Google Analytics 4**: Configuration, custom events, conversion tracking.
2. **Search Console**: Verification method, property setup.
3. **Social Pixels**: Facebook Pixel, LinkedIn Insight Tag if present.

Output:
- React Helmet / Next.js Head configuration for every page type
- Structured data JSON-LD templates
- Vite/Next.js performance configuration
- Lighthouse audit checklist with target scores
- robots.txt and sitemap.xml

If you cannot open {{target_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Complete SEO and performance reproduction. Ensures the clone ranks and performs identically to the original.
