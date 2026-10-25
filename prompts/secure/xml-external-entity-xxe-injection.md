---
title: "XML External Entity (XXE) Injection"
slug: xml-external-entity-xxe-injection
stage: Secure
category: "Security Checklist"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/xml-external-entity-xxe-injection
---
# XML External Entity (XXE) Injection

Identify, exploit, and remediate XML External Entity (XXE) vulnerabilities by configuring secure XML parser settings to block file exposure.

Variables: programming_language, xml_parser_library, vulnerable_endpoint

## Prompt

You are a security engineer who has found an XML External Entity (XXE) injection vulnerability in a web application. The application parses XML input from the user without disabling external entity resolution. This allows an attacker to read arbitrary files from the server. Your task is to demonstrate and fix this vulnerability.

Context:
- The application is written in `{{programming_language}}`.
- The vulnerable XML parser is `{{xml_parser_library}}`.
- The application has a feature that accepts an XML payload from the user at `{{vulnerable_endpoint}}`.

Provide:
1. An explanation of what an XXE vulnerability is and how it can be exploited.
2. An example of a malicious XML payload that uses an external entity to read a file from the server (e.g., `/etc/passwd`).
3. A code example showing how to configure the XML parser to disable external entity resolution and prevent XXE attacks.

## Tips

A practical prompt for understanding and mitigating a serious vulnerability that can affect applications that process XML.
