---
title: "Identify and Clean Up Unused Cloud Resources Defined in Infrastructure-as-Code"
slug: identify-and-clean-up-unused-cloud-resources-defined-in-infrastructure-as-code
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/identify-and-clean-up-unused-cloud-resources-defined-in-infrastructure-as-code
---
# Identify and Clean Up Unused Cloud Resources Defined in Infrastructure-as-Code

Get a guide to identifying and safely removing unused IaC cloud resources through static analysis, cloud usage tools, tagging, and deprecation.

Variables: iac_tool, cloud_provider

## Prompt

My organization uses `{{iac_tool}}` (e.g., Terraform, Pulumi) to manage our cloud infrastructure on `{{cloud_provider}}`. Over time, our IaC codebase has grown, and I suspect we are paying for cloud resources that are defined in our code but are no longer actually used by any application.

I need a strategy for identifying and safely removing this "infrastructure debt."

Your task is to provide a guide on how to do this.

1.  **The Problem of Unused Resources:** Explain the risks of unused IaC resources (e.g., cost, security surface, compliance drift).
2.  **Identification Strategy:** How can we identify unused resources? This is a hard problem. Propose a multi-pronged approach:
    *   **Static Analysis:** Are there tools that can analyze our `{{iac_tool}}` code and our application code to find resources that are defined but never referenced?
    *   **Cloud Provider Tools:** How can we use the tools provided by `{{cloud_provider}}` (e.g., AWS Cost Explorer, Azure Advisor) to find resources with zero traffic or usage?
    *   **Tagging:** Propose a tagging strategy where every resource is tagged with its owner and the application it belongs to. This makes it easier to identify orphaned resources.
3.  **Safe Removal Process:** Once we've identified a potentially unused resource (e.g., an S3 bucket, a database), what is a safe process for removing it?
    *   **Deprecation:** First, change its permissions to be read-only to see if anything breaks.
    *   **Backup:** Take a final backup or snapshot before deletion.
    *   **Deletion:** Use `{{iac_tool}}` to destroy the resource.
4.  **Prevention:** How can we prevent this from happening in the future? Suggest a process where new infrastructure requires a justification and an expiration date.

Output should be a strategic guide for managing the lifecycle of cloud infrastructure.

## Tips

A challenging but critical task for controlling cloud costs and reducing security risks.
