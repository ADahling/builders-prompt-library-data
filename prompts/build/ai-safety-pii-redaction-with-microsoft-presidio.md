---
title: "AI Safety: PII Redaction with Microsoft Presidio"
slug: ai-safety-pii-redaction-with-microsoft-presidio
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/ai-safety-pii-redaction-with-microsoft-presidio
---
# AI Safety: PII Redaction with Microsoft Presidio

Implement a Python script using Microsoft Presidio to redact PII and PHI from healthcare data to ensure HIPAA compliance before LLM processing.

## Prompt

As a data engineer in healthcare, you need to process patient feedback logs. Before sending these logs to an LLM for sentiment analysis, you must strictly redact all Personally Identifiable Information (PII) and Protected Health Information (PHI) to comply with HIPAA.

Your task is to write a Python script that uses the open-source 'presidio-analyzer' and 'presidio-anonymizer' libraries from Microsoft to redact PII from text.

**Scenario:**
- **Input Text:** "Patient John Doe, born on 05/12/1980, visited the clinic on Tuesday. His phone number is 555-0198 and email is j.doe@email.com. He complained of a headache."

**Technical Requirements:**
- The script must assume `presidio-analyzer`, `presidio-anonymizer`, and the spaCy model `en_core_web_lg` are installed.
- Initialize the `AnalyzerEngine` and `AnonymizerEngine`.
- Call the analyzer to detect entities in the input text. Specify that you want to find entities like `PERSON`, `PHONE_NUMBER`, `EMAIL_ADDRESS`, and `DATE_TIME`.
- Pass the analyzer results and the original text to the anonymizer.
- Configure the anonymizer to replace the detected entities with a placeholder, such as `<REDACTED>` or the entity type (e.g., `<PERSON>`).
- Print the original text and the safely redacted text to the console.

**Output Format:**
A complete, executable Python script demonstrating local PII redaction.
