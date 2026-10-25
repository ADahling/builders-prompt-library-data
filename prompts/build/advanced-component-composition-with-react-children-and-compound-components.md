---
title: "Advanced Component Composition with React Children and Compound Components"
slug: advanced-component-composition-with-react-children-and-compound-components
stage: Build
category: "Frontend & Styling"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-component-composition-with-react-children-and-compound-components
---
# Advanced Component Composition with React Children and Compound Components

Build compound React tabs for a design system in one TypeScript file, with Context-managed state, order-linked panels, and a usage example.

Variables: app_name

## Prompt

We are building a design system for our application, {{app_name}}, and need to create a highly reusable and flexible Tab component. The goal is to use the compound components pattern to give the developer full control over the structure and styling of the tabs.

The Tab component should be composed of a parent 'Tabs' component and child 'TabList', 'Tab', and 'TabPanel' components. The state (which tab is active) should be managed implicitly by the parent 'Tabs' component.

Your task is to:
1.  Create the set of compound components: 'Tabs', 'TabList', 'Tab', and 'TabPanel'.
2.  The 'Tabs' component will be the main container and state provider, using React Context to share the active tab state with its children.
3.  The 'TabList' will be a container for the 'Tab' buttons.
4.  Each 'Tab' component will be a button that, when clicked, updates the active tab state in the parent.
5.  Each 'TabPanel' will contain the content for a tab and will only be visible if its corresponding tab is active.
6.  The relationship between a 'Tab' and its 'TabPanel' should be established via their order.

Provide a complete implementation of this compound component system in a single TypeScript file. Include a usage example that shows how to compose a set of tabs with this system. The code should be well-structured and demonstrate a deep understanding of React's children, cloneElement, and Context API.
