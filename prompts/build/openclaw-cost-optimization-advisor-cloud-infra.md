---
title: "OpenClaw: Cost Optimization Advisor (Cloud/Infra)"
slug: openclaw-cost-optimization-advisor-cloud-infra
stage: Build
category: "OpenClaw"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-cost-optimization-advisor-cloud-infra
---
# OpenClaw: Cost Optimization Advisor (Cloud/Infra)

Review cloud bills or resource inventories for right-sizing options, unused resources, and short- to medium-term cost optimization steps.

Variables: budget

## Prompt

# Cost Optimization Advisor — Cloud & Infrastructure

## Input
Provide:
- Cloud provider billing export (AWS Cost Explorer, GCP Billing, Azure Cost Management)
- OR list of running resources with types and sizes
- Monthly budget target: {{budget}}

## Analysis Framework

### Resource Right-Sizing
| Resource Type | Check | Optimization |
|--------------|-------|-------------|
| Compute (EC2/GCE/VM) | CPU <20% avg, Memory <40% avg | Downsize instance type |
| Database (RDS/Cloud SQL) | CPU <15%, connections <30% of max | Downsize or switch to serverless |
| Storage (S3/GCS) | Access patterns, lifecycle | Move infrequent data to cold tier |
| Load Balancer | Requests/sec vs capacity | Consolidate or remove unused |
| NAT Gateway | Data transfer volume | Use VPC endpoints for AWS services |

### Quick Wins (implement in <1 day)
1. Delete unattached EBS volumes / persistent disks
2. Remove unused Elastic IPs / static IPs
3. Stop non-production resources outside business hours
4. Delete old snapshots (>90 days)
5. Review and cancel unused Reserved Instances

### Medium-Term (implement in 1-4 weeks)
1. Reserved Instances / Committed Use Discounts (1yr or 3yr)
2. Spot/Preemptible instances for fault-tolerant workloads
3. Auto-scaling policies based on actual usage patterns
4. Container right-sizing (CPU/memory requests vs actual)
5. CDN optimization for static assets

### Architecture-Level (1-3 months)
1. Serverless migration for bursty workloads
2. Multi-region consolidation
3. Database query optimization (reduce compute needs)
4. Caching layer to reduce origin requests
5. Data pipeline optimization (reduce processing costs)

## Output
- Current monthly spend breakdown
- Projected savings per recommendation
- Implementation priority (ROI × effort)
- Risk assessment for each change

## Tips

Cloud cost optimization with resource right-sizing, quick wins, and architecture-level recommendations. Works with AWS, GCP, and Azure.
