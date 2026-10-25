---
title: "Design System Token Architecture"
slug: design-system-token-architecture
stage: Design
category: "UX/UI Design"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-system-token-architecture
---
# Design System Token Architecture

Architect a multi-brand, cross-platform design token system with semantic naming, structured scales, and multi-language implementation code.

Variables: brand_name, number_of_products, number_of_brand_variants

## Prompt

You are a design systems architect. Create a comprehensive design token architecture for {{brand_name}} that supports {{number_of_products}} products across web and mobile.

Requirements:
- Support light and dark themes
- Support {{number_of_brand_variants}} brand variants
- Must be platform-agnostic (CSS, iOS, Android)
- Must support semantic naming

Provide:
1. **Token Hierarchy**: Global tokens -> Alias tokens -> Component tokens
2. **Color System**: Primitive palette, semantic colors, interactive states
3. **Typography Scale**: Font families, sizes, weights, line heights
4. **Spacing Scale**: Base unit, spacing tokens, layout tokens
5. **Elevation System**: Shadow tokens for depth
6. **Motion Tokens**: Duration, easing, transition presets
7. **Implementation**: Show how tokens translate to CSS custom properties, Tailwind config, and Swift/Kotlin
8. **Governance**: How to propose, review, and ship token changes

## Tips

Foundation for any multi-product design system. Start here before building components.
