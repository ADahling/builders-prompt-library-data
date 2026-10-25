---
title: "Network Security Review for a Kubernetes Cluster"
slug: network-security-review-for-a-kubernetes-cluster
stage: Secure
category: "Security Review"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/network-security-review-for-a-kubernetes-cluster
---
# Network Security Review for a Kubernetes Cluster

Conduct a comprehensive network security audit of a Kubernetes cluster to identify vulnerabilities and implement hardened traffic controls.

Variables: cloud_provider

## Prompt

You are a network security engineer responsible for securing a new Kubernetes cluster deployed on {{cloud_provider}}. The cluster will host a variety of microservices, some of which are internet-facing. Your task is to review the network security of the cluster and recommend best practices.

Create a detailed network security review report in Markdown. The report should cover the following areas:

1.  **Network Policies:**
    *   Review the use of Kubernetes network policies to control traffic flow between pods.
    *   Provide an example of a default-deny network policy and a more permissive policy for a specific application.
2.  **Ingress and Egress Control:**
    *   Review the configuration of the Ingress controller. Ensure that it is configured to use TLS and that it is not exposing any unnecessary services.
    *   Recommend a solution for controlling egress traffic from the cluster to prevent data exfiltration.
3.  **Control Plane Security:**
    *   Review the security of the Kubernetes API server. Ensure that it is not publicly exposed and that access is restricted to authorized users.
4.  **Node Security:**
    *   Review the security of the worker nodes. Ensure that they are running a hardened OS and that access to the nodes is restricted.
5.  **Service Mesh Security:**
    *   If a service mesh like Istio or Linkerd is being used, review its security configuration. Ensure that mTLS is enabled for all service-to-service communication.

For each area, provide your assessment of the current configuration and a list of prioritized recommendations for improvement. Your report should be a practical guide for the platform engineering team to secure the Kubernetes cluster.
