---
title: "Building a Translation Agent"
slug: building-a-translation-agent
stage: Build
category: "AI Agent Development"
grade: C
score: 69
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-translation-agent
---
# Building a Translation Agent

Get a Python translation chain that detects the source language and returns formatted translated text in a chosen target language.

Variables: text, target_language

## Prompt

Create a simple AI agent dedicated to translating text between languages. While an LLM can do this directly, wrapping it in an agent structure allows you to add pre- and post-processing steps.

**Agent Features:**

1.  **Language Detection:** The agent should automatically detect the source language if it's not provided.
2.  **Translation:** Translate the text to the target language.
3.  **Formatting:** Ensure the output is formatted cleanly.

**Implementation:**

1.  **Prompt Template:** Create a prompt template that takes `{{text}}` and `{{target_language}}`. The prompt should instruct the LLM to:
    *   Identify the source language.
    *   Translate the text.
    *   Output the result in a specific format, e.g., "Source: [Language]
Translation: [Translated Text]".
2.  **Chain:** Create an LLM chain with this prompt.
3.  **Execution:** Run the chain with a sample text and target language.

**Example Input:**

*   Text: "Bonjour, comment ça va?"
*   Target Language: "English"

**Output:**

A simple Python script demonstrating this translation chain.
