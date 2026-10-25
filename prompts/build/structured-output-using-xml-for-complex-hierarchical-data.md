---
title: "Structured Output: Using XML for Complex Hierarchical Data"
slug: structured-output-using-xml-for-complex-hierarchical-data
stage: Build
category: "LLM & AI Integration"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/structured-output-using-xml-for-complex-hierarchical-data
---
# Structured Output: Using XML for Complex Hierarchical Data

Transform natural language order requests into strictly formatted, schema-compliant XML for legacy enterprise system integration.

## Prompt

You are integrating with an old enterprise system that requires all data to be exchanged in a specific, complex XML format. You need to use an LLM to generate an XML document from a natural language request.

Your task is to create a prompt for an LLM (like Claude Sonnet 5) that is highly effective at generating structured XML.

**Scenario:**
- **User Request:** "Create a new order for customer ID 123. The order should contain two items: a 'Laptop' with SKU 'LP100' and price '1500', and a 'Mouse' with SKU 'MS200' and price '50'. The shipping address is 123 Main St, Anytown."
- **Desired XML Output:**
`<order>
  <customer_id>123</customer_id>
  <shipping_address>123 Main St, Anytown</shipping_address>
  <items>
    <item sku="LP100">
      <name>Laptop</name>
      <price>1500</price>
    </item>
    <item sku="MS200">
      <name>Mouse</name>
      <price>50</price>
    </item>
  </items>
</order>`

**Prompt Engineering Task:**
You are not writing code, but the prompt itself.

**Prompt Requirements:**
1.  **Role Definition:** "You are a strict and precise data formatting engine. Your only purpose is to convert natural language into valid XML."
2.  **The Task:** "Your task is to convert the following user order into the specified XML format."
3.  **Input Data:** Provide the user's request.
4.  **Schema Definition (Crucial for XML):** "The output must be a valid XML document that conforms to the following structure. Provide the exact XML structure as an example for the model to follow:
    [Paste the desired XML output structure here]
    Pay close attention to attributes (like 'sku') versus elements (like 'name')."
5.  **Constraints:** "The output must be a single, well-formed XML block. Do not include any extra text, explanations, or the `<?xml version="1.0"?>` prolog. Start directly with the `<order>` tag."

**Output Format:**
Provide a single block of text representing the complete, final prompt that would be sent to the LLM.
