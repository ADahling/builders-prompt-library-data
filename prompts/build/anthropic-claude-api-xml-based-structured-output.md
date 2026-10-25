---
title: "Anthropic Claude API: XML-based Structured Output"
slug: anthropic-claude-api-xml-based-structured-output
stage: Build
category: "LLM & AI Integration"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/anthropic-claude-api-xml-based-structured-output
---
# Anthropic Claude API: XML-based Structured Output

Generate a Python script using the Anthropic SDK to extract customer feedback into structured XML using Claude Opus 4.8.

## Prompt

You are a data analyst tasked with processing customer feedback. You need to use Anthropic's Claude Opus 4.8 to extract specific pieces of information from feedback emails and structure them within XML tags.

Your goal is to create a Python script that sends a customer email to the Claude API and asks it to wrap key information in predefined XML tags.

**Customer Email:**
"I recently purchased the 'Pro-Blender 5000' (Order #A987-2) and I'm very happy with its performance. However, the lid doesn't seem to fit securely. I'd rate the product a 4 out of 5 overall. The delivery was also very fast."

**Desired XML Output Structure:**
```xml
<feedback>
  <product_name>Pro-Blender 5000</product_name>
  <order_id>A987-2</order_id>
  <sentiment>Positive</sentiment>
  <rating>4/5</rating>
  <issue>The lid doesn't seem to fit securely.</issue>
</feedback>
```

**Technical Requirements:**
- Use the 'anthropic' Python SDK and the 'claude-opus-4-8-2026' model.
- The prompt sent to Claude must be very specific. It should provide the customer email and instruct the model to extract the relevant data and format it using the exact XML structure shown above. You should provide the XML structure as an example in the prompt.
- The script should then print the raw XML string returned by Claude to the console.
- The prompt should also instruct Claude to output *only* the XML block and nothing else.

**Output Format:**
A single, runnable Python script.
