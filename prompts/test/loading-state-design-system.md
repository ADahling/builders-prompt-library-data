---
title: "Loading State Design System"
slug: loading-state-design-system
stage: Test
category: "UX/UI Fixes"
grade: A+
score: 94
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/loading-state-design-system
---
# Loading State Design System

Generate a comprehensive React and Tailwind-based loading system featuring skeleton screens, optimistic updates, and accessible error handling.

Variables: application_name, components_list

## Prompt

You are a UX engineer. Design a comprehensive loading state system for {{application_name}}.

Pages/components that need loading states:
{{components_list}}

Design:
1. **Skeleton Screens**: Shimmer skeletons that match the final layout for each component
2. **Spinner Variants**: When to use spinner vs skeleton vs progress bar
3. **Progressive Loading**: Show content as it becomes available (don't wait for everything)
4. **Error States**: What to show when loading fails (retry button, helpful message)
5. **Empty States**: What to show when data loads but is empty
6. **Optimistic Updates**: Update UI immediately, rollback on failure
7. **Timeout Handling**: What to show after 5s, 10s, 30s of loading
8. **Offline State**: What to show when the user loses connection

For each state, provide:
- React component code with Tailwind styling
- Animation (subtle pulse or shimmer)
- Accessibility (aria-busy, aria-live announcements)
- Transition animation from loading to loaded

## Tips

Perceived performance matters more than actual performance. Good loading states make apps feel faster.
