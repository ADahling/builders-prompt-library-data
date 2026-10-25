---
title: "Create a Render Prop Component for Mouse Position Tracking in React"
slug: create-a-render-prop-component-for-mouse-position-tracking-in-react
stage: Build
category: "Frontend & Styling"
grade: A+
score: 93
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-render-prop-component-for-mouse-position-tracking-in-react
---
# Create a Render Prop Component for Mouse Position Tracking in React

Implement a TypeScript-based React render prop component that tracks and exposes real-time mouse coordinates for interactive UI elements.

Variables: tech_stack

## Prompt

I am building a data visualization dashboard in React ({{tech_stack}}) and need a reusable component that tracks the user's mouse position within a specific container. This functionality will be used to display tooltips and interactive elements that follow the cursor.

Create a React component named MousePositionTracker that uses the render prop pattern. This component should not render any UI itself but will provide the current mouse coordinates (x, y) to its children.

The MousePositionTracker component must:
1.  Accept a render prop as its child, which is a function that receives the mouse coordinates.
2.  Attach and clean up mouse move event listeners to the window object efficiently.
3.  Update the state with the new coordinates whenever the mouse moves.
4.  Pass the coordinates as an object { x: number, y: number } to the render prop function.
5.  The component should be written in TypeScript, with clear type definitions for its props and state.

Provide a complete implementation of the MousePositionTracker component and a usage example. The example should show how to use the component to display the current mouse coordinates on the screen. The output should be a single TypeScript file with all the necessary code.
