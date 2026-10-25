---
title: "Structured Output: Generating CSV from Unstructured Text"
slug: structured-output-generating-csv-from-unstructured-text
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/structured-output-generating-csv-from-unstructured-text
---
# Structured Output: Generating CSV from Unstructured Text

Extract sales data from unstructured text and format it into a clean, schema-aligned CSV for direct use in spreadsheet applications.

## Prompt

You are a data analyst and have been given a block of unstructured text describing sales transactions. You need to convert this into a structured CSV format for analysis in a spreadsheet program.

Your task is to create a prompt for an LLM that can reliably perform this conversion.

**Scenario:**
- **Input Text:** "On Monday, we sold 3 widgets to customer A for $30. Then, on Tuesday, customer B bought 5 widgets for $50. Finally, customer C purchased 1 widget for $10 on Wednesday."
- **Desired CSV Output:**
`Day,Customer,Quantity,Total_Price
Monday,Customer A,3,30
Tuesday,Customer B,5,50
Wednesday,Customer C,1,10`

**Prompt Engineering Task:**
You are not writing code, but the prompt itself.

**Prompt Requirements:**
1.  **Role Definition:** "You are an expert data extraction and formatting tool."
2.  **The Task:** "Your task is to convert the following unstructured text into a valid CSV format."
3.  **Input Data:** Provide the input text.
4.  **Schema Definition:** "The CSV must have the following header row: `Day,Customer,Quantity,Total_Price`."
5.  **Constraints:** "Extract the data and format it precisely according to the header. Do not include any extra text, explanations, or markdown formatting. The output should be the raw CSV content, starting with the header row."

**Output Format:**
Provide a single block of text representing the complete, final prompt that would be sent to the LLM.
