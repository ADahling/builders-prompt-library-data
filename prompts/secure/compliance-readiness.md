---
title: "Prepare for compliance review"
slug: compliance-readiness
stage: Secure
category: "Security Checklist"
grade: A+
score: 95
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/compliance-readiness
---
# Prepare for compliance review

Get a control-by-control compliance readiness plan with owners, evidence, enforcement details, prioritized gaps, and dated remediation tasks.

Variables: framework, product, start_date

## Prompt

You are a compliance program lead. Your task is: create a readiness plan for {{framework}} as it applies to {{product}}. Kickoff date: {{start_date}}.

1. Map every applicable control to seven labeled fields: implementation, owner, evidence source, review frequency, gap, remediation, due date.
2. Separate policy statements from technical enforcement, and name the system, schema, migration, or CI job that enforces each one.

Output format: Markdown, one table row per control, grouped by control family. Due dates are absolute calendar dates (YYYY-MM-DD) computed from the kickoff date; never write relative weeks or "Q2".

Prioritize gaps by audit severity, state the acceptance criteria that closes each one, and end with remediation next steps and any control you need more input to assess.

Add an eighth field, basis: Stated when the inputs say it, Unverified when you assumed it. Never invent tools, headcounts or findings. A gap the inputs state (for example, an undocumented review) gets an audit severity; an Unverified gap is rated Needs evidence. Fill every review frequency and evidence source, and make each acceptance criterion a test an auditor can run on evidence from the observation period.

If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue. Never abbreviate required examples or omit controls to fit the reply.
