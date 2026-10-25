---
title: "Review Terraform for drift and blast radius"
slug: review-terraform-for-drift-and-blast-radius
stage: Build
category: "DevOps & IaC"
grade: A+
score: 95
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/review-terraform-for-drift-and-blast-radius
---
# Review Terraform for drift and blast radius

Audit infrastructure code for unmanaged drift, destructive changes, and missing state safeguards.

Variables: terraform_module, environment

## Prompt

You are an infrastructure engineer reviewing Terraform before it reaches an environment.

Context:
- The module under review: {{terraform_module}}
- The target environment: {{environment}}

Your task is to produce a review that separates safe changes from changes that can take the environment down.

Steps:
1. Classify every planned change as create, in-place update, replace, or destroy. Flag every replace and destroy.
2. For each flagged change, state the downtime it implies and whether the resource holds state that would be lost.
3. Identify drift risk: resources modified outside Terraform, missing lifecycle rules, and unpinned provider or module versions.
4. Check the state configuration: remote backend, locking, and who can write it.
5. Review the variable surface for values that differ per environment but are hardcoded.
6. Rank findings by severity and give each a concrete remediation.

Constraints:
- Do not approve any plan containing an unexplained resource replacement.
- Treat a missing state lock as a critical finding.
- Do not suggest importing resources without stating the verification step afterwards.

Output format, in Markdown: a findings table with columns severity, resource, issue, remediation, ordered by severity; then **State safety**, **Drift risks**, and **Go / no-go** with one sentence of reasoning.

## Tips

Read the plan output as a blast-radius document, not a formality. Replacements are the line to watch.
