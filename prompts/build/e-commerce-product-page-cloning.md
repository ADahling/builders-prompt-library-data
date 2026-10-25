---
title: "E-Commerce Product Page Cloning"
slug: e-commerce-product-page-cloning
stage: Build
category: "Website Cloning"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/e-commerce-product-page-cloning
---
# E-Commerce Product Page Cloning

Replicate high-conversion e-commerce layouts by building a responsive, accessible React product page with variant management and SEO.

Variables: target_ecommerce_site, new_store_name

## Prompt

You are a frontend developer specializing in e-commerce. Clone the product page layout of {{target_ecommerce_site}} for {{new_store_name}}.

Elements to clone:
- Product image gallery (zoom, thumbnails, mobile swipe)
- Product title, price, variants (size, color)
- Add to cart button with quantity selector
- Product description tabs (Description, Reviews, Shipping)
- Related products carousel
- Trust badges and shipping information

Provide:
1. **Component Architecture**: Break down into reusable React components
2. **Image Gallery**: Responsive gallery with zoom, thumbnails, and mobile swipe
3. **Variant Selector**: Dynamic price updates based on selected variant
4. **Add to Cart**: Optimistic UI with cart drawer animation
5. **Reviews Section**: Star ratings, review cards, pagination
6. **Responsive Design**: Mobile-first with Tailwind breakpoints
7. **SEO**: Structured data (JSON-LD) for product schema
8. **Performance**: Image lazy loading, skeleton loading states
9. **Accessibility**: ARIA labels, keyboard navigation, screen reader support
10. **Animation**: Subtle micro-interactions (hover effects, transitions)

If you cannot open {{target_ecommerce_site}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Product pages are the highest-converting pages on any e-commerce site. Every pixel matters.
