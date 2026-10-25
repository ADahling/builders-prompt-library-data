---
title: "Kubernetes Cost Optimization Audit"
slug: kubernetes-cost-optimization-audit
stage: Test
category: "Quality Audits"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/kubernetes-cost-optimization-audit
---
# Kubernetes Cost Optimization Audit

Conduct a comprehensive Kubernetes audit to identify resource inefficiencies and implement autoscaling, spot instances, and governance strategies.

Variables: project_name

## Prompt

As a cloud cost management expert, I need you to conduct a cost optimization audit of our Kubernetes cluster for the project `{{project_name}}`. Our monthly cloud spending has been increasing, and we need to identify opportunities to reduce costs without impacting performance or availability.

Your audit should analyze our Kubernetes usage and spending, and provide actionable recommendations for cost optimization. The audit should cover the following areas:

1.  **Resource Utilization:**
    *   Identify any underutilized or idle resources, such as nodes, pods, and persistent volumes.
    *   Provide recommendations for rightsizing resources to match their actual workload.

2.  **Cluster Autoscaling:**
    *   Analyze our cluster autoscaling configuration and provide recommendations for optimizing it.

3.  **Pod Autoscaling:**
    *   Analyze our horizontal and vertical pod autoscaling configurations and provide recommendations for optimizing them.

4.  **Spot Instances:**
    *   Analyze our usage patterns and provide recommendations for using spot instances to reduce costs.

5.  **Automation and Governance:**
    *   Provide recommendations for implementing cost management tools and automation to help us better track and control our Kubernetes spending.
    *   Suggest cost allocation and tagging strategies to improve visibility into our spending.

**Output Format:**

Please provide a Kubernetes cost optimization audit report in a Markdown file with the following structure:

*   **Cost Savings Summary:** A high-level overview of the potential cost savings identified in the audit.
*   **Cost Optimization Recommendations:** A prioritized list of recommendations for reducing our Kubernetes costs. For each recommendation, provide:
    *   **Recommendation ID:** A unique identifier.
    *   **Area:** (e.g., Nodes, Pods, Storage)
    *   **Potential Savings:** An estimate of the potential monthly cost savings.
    *   **Implementation Effort:** (Low, Medium, High)
    *   **Detailed Steps:** A clear, step-by-step guide on how to implement the recommendation.
*   **Cost Management Best Practices:** A list of best practices for ongoing Kubernetes cost management.
