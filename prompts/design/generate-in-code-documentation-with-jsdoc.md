---
title: "Generate In-Code Documentation with JSDoc"
slug: generate-in-code-documentation-with-jsdoc
stage: Design
category: "Documentation"
grade: A
score: 84
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-in-code-documentation-with-jsdoc
---
# Generate In-Code Documentation with JSDoc

Enhance JavaScript functions with comprehensive JSDoc comments to improve API readability, IDE support, and automated documentation generation.

## Prompt

You are a senior JavaScript developer who believes in the power of self-documenting code. You are working on a new Node.js module and want to add JSDoc comments to all your functions to automatically generate API documentation.

Your task is to take the following JavaScript function and add a comprehensive JSDoc comment block. The comment should include:

*   A brief description of what the function does.
*   `@param` tags for each parameter, specifying its type, name, and a description.
*   `@returns` tag, specifying the type and a description of the return value.
*   `@throws` tag for any errors the function might throw.
*   `@example` tag with a clear code example of how to use the function.

Here is the function to document:

`
function calculateTotalPrice(items, taxRate, discount) {
  if (!Array.isArray(items)) {
    throw new Error('Items must be an array of objects.');
  }
  const subtotal = items.reduce((acc, item) => acc + item.price * item.quantity, 0);
  const tax = subtotal * taxRate;
  const total = subtotal + tax - discount;
  return total;
}
`

Generate the complete function with the JSDoc comment block.
