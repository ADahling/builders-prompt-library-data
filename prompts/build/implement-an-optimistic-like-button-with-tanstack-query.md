---
title: "Implement an Optimistic Like Button with TanStack Query"
slug: implement-an-optimistic-like-button-with-tanstack-query
stage: Build
category: "Frontend & Styling"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-an-optimistic-like-button-with-tanstack-query
---
# Implement an Optimistic Like Button with TanStack Query

Get a TanStack Query useMutation example for a post like button with immediate UI updates, background requests, and rollback on failure.

## Prompt

I'm building a web application that needs to support optimistic updates for a better user experience. I'm using TanStack Query (formerly React Query) for data fetching. I want to implement an optimistic update for a 'like' feature on a post. When the user clicks the 'like' button, the UI should update immediately, and the actual API request should be sent in the background. If the request fails, the UI should revert to its original state. Provide a complete example of how to implement an optimistic update with `useMutation` from TanStack Query. The example should include the mutation function, the `onMutate` and `onError` callbacks, and the component that uses the mutation..
