---
title: "Optimize Webpack Bundle Size and Tree Shaking"
slug: optimize-webpack-bundle-size-and-tree-shaking
stage: Test
category: "Performance & Code"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-webpack-bundle-size-and-tree-shaking
---
# Optimize Webpack Bundle Size and Tree Shaking

Get a guide for large React bundles with Webpack analysis, tree shaking, side-effect settings, plugins, and Webpack and Babel config examples.

Variables: AppName

## Prompt

Our React application, `{{AppName}}`, is suffering from a large bundle size, which is negatively impacting our Lighthouse performance score. I need you to act as a Webpack expert and provide a comprehensive guide to optimizing our bundle size through effective tree shaking and other Webpack configurations.

Your response should be a detailed set of instructions that I can follow to analyze and reduce our bundle size. Please include the following:
1.  **Bundle Analysis:** Instructions on how to use `webpack-bundle-analyzer` to visualize our bundle and identify large or unused dependencies.
2.  **Tree Shaking Configuration:** A clear explanation of how to configure Webpack and Babel to ensure that tree shaking is working correctly for both our application code and third-party libraries.
3.  **Side Effect-Free Modules:** Guidance on how to mark modules as side-effect-free in our `package.json` to improve tree shaking.
4.  **Plugin Recommendations:** A list of Webpack plugins that can help further reduce the bundle size, such as `TerserWebpackPlugin` for minification and `CompressionWebpackPlugin` for gzipping.
5.  **Example Configurations:** Provide example snippets for `webpack.config.js` and `.babelrc` that demonstrate the recommended configurations.
