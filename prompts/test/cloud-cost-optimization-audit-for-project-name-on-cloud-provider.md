---
title: "Cloud Cost Optimization Audit"
slug: cloud-cost-optimization-audit-for-project-name-on-cloud-provider
stage: Test
category: "Quality Audits"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cloud-cost-optimization-audit-for-project-name-on-cloud-provider
---
# Cloud Cost Optimization Audit

Audit rising cloud costs with recommendations for resource sizing, savings plans, storage tiers, networking, and cost governance.

Variables: project_name, cloud_provider

## Prompt

As a cloud cost management expert, I need you to conduct a cost optimization audit of our cloud infrastructure for the project `{{project_name}}` on {{cloud_provider}}. Our monthly cloud spending has been increasing, and we need to identify opportunities to reduce costs without impacting performance or availability.

Your audit should analyze our cloud usage and spending, and provide actionable recommendations for cost optimization. The audit should cover the following areas:

1.  **Resource Utilization:**
    *   Identify any underutilized or idle resources, such as virtual machines, databases, and storage.
    *   Provide recommendations for rightsizing resources to match their actual workload.

2.  **Reserved Instances and Savings Plans:**
    *   Analyze our usage patterns and provide recommendations for purchasing reserved instances or savings plans to reduce costs.

3.  **Storage Optimization:**
    *   Review our storage usage and identify opportunities to move data to lower-cost storage tiers.
    *   Provide recommendations for implementing data lifecycle policies to automatically manage storage costs.

4.  **Networking Costs:**
    *   Analyze our data transfer costs and identify any opportunities to reduce them.

5.  **Automation and Governance:**
    *   Provide recommendations for implementing cost management tools and automation to help us better track and control our cloud spending.
    *   Suggest cost allocation and tagging strategies to improve visibility into our spending.

**Output Format:**

Please provide a cloud cost optimization audit report in a Markdown file with the following structure:

*   **Cost Savings Summary:** A high-level overview of the potential cost savings identified in the audit.
*   **Cost Optimization Recommendations:** A prioritized list of recommendations for reducing our cloud costs. For each recommendation, provide:
    *   **Recommendation ID:** A unique identifier.
    *   **Area:** (e.g., Compute, Storage, Networking)
    *   **Potential Savings:** An estimate of the potential monthly cost savings.
    *   **Implementation Effort:** (Low, Medium, High)
    *   **Detailed Steps:** A clear, step-by-step guide on how to implement the recommendation.
*   **Cost Management Best Practices:** A list of best practices for ongoing cloud cost management.
