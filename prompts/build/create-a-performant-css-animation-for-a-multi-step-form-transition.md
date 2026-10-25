---
title: "Create a Performant CSS Animation for a Multi-step Form Transition"
slug: create-a-performant-css-animation-for-a-multi-step-form-transition
stage: Build
category: "Frontend & Styling"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-performant-css-animation-for-a-multi-step-form-transition
---
# Create a Performant CSS Animation for a Multi-step Form Transition

Get CSS and sample HTML for sliding transitions in a React multi-step form, with directional classes and transform-based animations.

Variables: app_name

## Prompt

I'm working on a user registration flow for {{app_name}}, which is a multi-step form. To improve the user experience, I want to add smooth transitions between the steps. The form is built with React.

Your task is to create a CSS animation that slides the form steps in and out of view. When the user clicks 'Next', the current step should slide out to the left, and the next step should slide in from the right. When they click 'Previous', the reverse should happen.

The animation should:
1.  Be implemented using only CSS transitions and animations. Avoid using JavaScript for the animation logic itself (JS can be used to toggle classes).
2.  Be performant, using hardware-accelerated properties like 'transform' and 'opacity' instead of affecting layout properties like 'margin' or 'left'.
3.  Define a set of CSS classes (e.g., 'form-step-enter', 'form-step-exit-active') that can be applied to the form step components to trigger the animations.
4.  The animation should have a duration of approximately 300ms and use an 'ease-in-out' timing function.

Provide the complete CSS code for the animations. Also, include a brief explanation and a simple HTML structure to demonstrate how the classes would be applied to the form steps during the transition. You can assume a React component would manage adding and removing these classes.
