---
title: "SaaS Dashboard Cloning Framework"
slug: saas-dashboard-cloning-framework
stage: Build
category: "Website Cloning"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/saas-dashboard-cloning-framework
---
# SaaS Dashboard Cloning Framework

Replicate a specific SaaS dashboard's UI architecture into a responsive React and Tailwind implementation using a structured 10-point framework.

Variables: target_saas, new_application, dashboard_elements

## Prompt

You are a frontend architect specializing in dashboard design. Clone the dashboard UI of {{target_saas}} for {{new_application}}.

Elements to clone:
- {{dashboard_elements}}

Cloning framework:
1. **Layout Analysis**: Grid system, sidebar width, content area proportions
2. **Navigation Pattern**: Sidebar nav, breadcrumbs, tab navigation
3. **Data Display**: Tables, charts, cards, metrics panels
4. **Interactive Elements**: Filters, date pickers, search, bulk actions
5. **Responsive Behavior**: How the dashboard adapts to tablet and mobile
6. **Color System**: Extract the exact color palette and map to Tailwind
7. **Typography**: Font families, sizes, weights, line heights
8. **Spacing System**: Consistent padding, margins, gaps
9. **Component Library**: Map each UI element to shadcn/ui or custom components
10. **State Management**: How data flows through the dashboard

Provide:
- Complete React + TypeScript + Tailwind implementation
- Responsive breakpoints
- Mock data that matches the original's data density
- Dark mode variant

## Tips

Dashboard cloning is about understanding the information architecture, not just copying pixels.
