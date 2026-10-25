---
title: "Optimize Web Performance with Code Splitting and Lazy Loading in a React Application"
slug: optimize-web-performance-with-code-splitting-and-lazy-loading-in-a-react-application
stage: Build
category: "Frontend & Styling"
grade: A+
score: 95
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-web-performance-with-code-splitting-and-lazy-loading-in-a-react-application
---
# Optimize Web Performance with Code Splitting and Lazy Loading in a React Application

Get before-and-after React routing examples in one TypeScript file, using React.lazy and Suspense to split page code for a slow-loading SPA.

Variables: app_name

## Prompt

Our React single-page application (SPA), {{app_name}}, has grown large, and its initial load time is suffering due to a large JavaScript bundle. We need to implement code splitting and lazy loading to improve performance.

Your task is to refactor the application's routing to use code splitting. The application has three main sections: a Dashboard, a Profile page, and a Settings page.

The refactoring should:
1.  Use React.lazy() to dynamically import the components for the Dashboard, Profile, and Settings pages.
2.  Wrap the lazy-loaded components in a React.Suspense component to show a loading fallback UI (e.g., a spinner) while the component code is being fetched.
3.  Assume the application uses React Router for its routing. The routes should be configured to render the lazy-loaded components.
4.  The goal is to split the code for each page into a separate chunk, so the user only downloads the code for the page they are visiting.

Provide a complete, before-and-after example of the main App component that sets up the routing. The 'before' example should show the traditional, static import of components. The 'after' example should demonstrate the implementation of lazy loading and Suspense. The output should be in a single TypeScript file.
