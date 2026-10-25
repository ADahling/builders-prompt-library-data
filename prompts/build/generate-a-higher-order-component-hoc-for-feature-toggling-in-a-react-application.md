---
title: "Generate a Higher-Order Component (HOC) for Feature Toggling in a React Application"
slug: generate-a-higher-order-component-hoc-for-feature-toggling-in-a-react-application
stage: Build
category: "Frontend & Styling"
grade: A+
score: 95
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-higher-order-component-hoc-for-feature-toggling-in-a-react-application
---
# Generate a Higher-Order Component (HOC) for Feature Toggling in a React Application

Create a TypeScript HOC that conditionally renders React components by consuming feature flags from a context-based configuration system.

Variables: tech_stack

## Prompt

As a senior frontend developer, I need to implement a feature flagging system in our React application, which is built with {{tech_stack}}. The goal is to conditionally render components or features based on a set of feature flags loaded from a remote configuration service.

Generate a Higher-Order Component (HOC) named withFeatureToggle that takes a component and a feature flag name as arguments. The HOC should handle the logic of checking if the feature is enabled and only render the wrapped component if the flag is active. The feature flags are available through a React context called FeatureFlagsContext.

Your HOC should:
1.  Consume the feature flags from FeatureFlagsContext.
2.  Accept the wrapped component and the required feature flag name as props.
3.  Conditionally render the wrapped component based on whether the feature flag is true.
4.  If the flag is not present or false, the HOC should render nothing (null).
5.  Include comprehensive JSDoc comments explaining how to use the HOC, its parameters, and what it returns.
6.  The code should be written in TypeScript and follow our company's coding standards, which emphasize readability and strong typing.

Provide a complete code example, including the HOC implementation, a sample FeatureFlagsContext setup, and a usage example where a component is wrapped with the withFeatureToggle HOC. The context should provide an object of feature flags, like { 'new-dashboard': true, 'beta-feature': false }.

Output the code in a single, well-formatted TypeScript file.
