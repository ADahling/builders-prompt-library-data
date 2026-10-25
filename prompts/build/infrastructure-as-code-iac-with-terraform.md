---
title: "Infrastructure as Code (IaC) with Terraform"
slug: infrastructure-as-code-iac-with-terraform
stage: Build
category: "System Architecture"
grade: A
score: 81
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/infrastructure-as-code-iac-with-terraform
---
# Infrastructure as Code (IaC) with Terraform

Create a beginner-friendly Terraform guide to automate cloud infrastructure using declarative HCL and standard DevOps workflows.

Variables: cloud_provider

## Prompt

You are a DevOps engineer who wants to introduce the concept of Infrastructure as Code (IaC) to your team. You have chosen Terraform as the tool to manage your cloud infrastructure on {{cloud_provider}}.

**Your Task:**
Create a beginner-friendly guide to Infrastructure as Code using Terraform. The guide should explain the benefits and provide a simple, hands-on example.

**Instructions & Constraints:**
1.  **The Problem with Manual Infrastructure Management:**
    *   Explain the problems with managing cloud infrastructure manually through a web console (e.g., it's slow, error-prone, not repeatable, and impossible to track changes).

2.  **The Solution: Infrastructure as Code (IaC):**
    *   Explain what IaC is: managing and provisioning infrastructure through code and automation.
    *   Describe the key benefits of IaC: automation, repeatability, version control, and collaboration.

3.  **Introduction to Terraform:**
    *   Explain what Terraform is: an open-source IaC tool that lets you define your infrastructure in a declarative language called HCL (HashiCorp Configuration Language).
    *   Describe the core Terraform workflow: `init
