---
title: "OpenClaw: CRM Natural Language Access"
slug: openclaw-crm-natural-language-access
stage: Build
category: "OpenClaw"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-crm-natural-language-access
---
# OpenClaw: CRM Natural Language Access

CRM / Business Tool Natural Language Access Build a natural-language interface to your CRM HubSpot, Salesforce, etc.

## Prompt

# CRM / Business Tool Natural Language Access

Build a natural-language interface to your CRM (HubSpot, Salesforce, etc.).

## Supported Objects & Operations
- **Contacts:** search, create, update, list, get by ID
- **Companies:** search, create, update, list
- **Deals:** search, create, update, list, query by pipeline stage
- **Owners:** list
- **Associations:** link contacts↔companies, deals↔contacts, deals↔companies

## Intent Classification
Parse messages into operations:
1. **Lookup:** "Find the contact for Sarah Chen" → search contacts
2. **Create:** "Add a new contact: John, john@acme.com, Acme Corp" → create contact
3. **Update:** "Update Sarah's title to VP Engineering" → update contact
4. **List:** "Show all deals in negotiation stage" → filter deals
5. **Associate:** "Link Sarah to Acme Corp" → create association

## Validation
If required fields are missing, ask before proceeding.

## Response Format
Return clean, readable summaries — not raw JSON.
For deal queries include: deal name, amount, stage, close date, last modified.

## Authentication
API key or OAuth stored in environment variables. Never expose in responses.

## Tips

Natural language interface to CRM systems. Supports CRUD operations on contacts, companies, deals with intent classification. From mberman84's extended gist.
