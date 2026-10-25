---
title: "Create a Few-Shot Prompt for Generating Marketing Copy"
slug: create-a-few-shot-prompt-for-generating-marketing-copy
stage: Idea
category: "Prompt Engineering"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-few-shot-prompt-for-generating-marketing-copy
---
# Create a Few-Shot Prompt for Generating Marketing Copy

Engineer a few-shot prompt for a marketing copywriter that uses specific product details, tone, and examples to generate persuasive copy.

Variables: product_name, target_audience, tone

## Prompt

You are a marketing copywriter. Your task is to create a few-shot prompt to generate marketing copy for a new product. The prompt should provide the AI with a few examples of high-quality marketing copy for similar products to guide its output.

The prompt should include:

- **Product Description**: A detailed description of the new product, including its name ({{product_name}}), its features, and its target audience ({{target_audience}}).
- **Examples**: At least three examples of marketing copy for similar products. Each example should include a headline and a body.
- **Instructions**: Clear instructions for the AI to generate a new headline and body for the new product, based on the provided examples. The tone should be {{tone}} (e.g., playful, professional, urgent).

The goal is to generate creative and persuasive marketing copy that will resonate with the target audience.

## Tips

This prompt demonstrates the use of few-shot learning to guide an AI in generating high-quality, contextually relevant marketing copy.
