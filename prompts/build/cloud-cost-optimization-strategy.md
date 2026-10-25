---
title: "Cloud Cost Optimization Strategy"
slug: cloud-cost-optimization-strategy
stage: Build
category: "DevOps & IaC"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cloud-cost-optimization-strategy
---
# Cloud Cost Optimization Strategy

Plan cloud cost optimization for your infrastructure with a resource inventory, quick wins, longer-term changes, and budget monitoring.

## Prompt

Analyze my cloud infrastructure costs and create an optimization plan:

1. RESOURCE INVENTORY:
   - List all running resources with type, size, region, and monthly cost
   - Identify resources with low utilization (< 20% CPU/memory)
   - Find resources with no tags or unclear ownership

2. QUICK WINS (save money this week):
   - Stop unused development/staging resources outside business hours
   - Delete unattached storage volumes and old snapshots
   - Downsize over-provisioned instances
   - Remove unused elastic IPs and load balancers

3. MEDIUM-TERM OPTIMIZATIONS:
   - Reserved instances or savings plans for stable workloads
   - Spot instances for fault-tolerant workloads
   - Right-sizing based on actual usage data
   - Storage tiering (move cold data to cheaper storage)

4. ARCHITECTURE OPTIMIZATIONS:
   - Serverless where appropriate (Lambda, Edge Functions)
   - Caching to reduce compute and database load
   - CDN for static assets
   - Connection pooling for databases

5. MONITORING & GOVERNANCE:
   - Budget alerts at 50%, 80%, 100% of target
   - Cost anomaly detection
   - Tagging policy enforcement
   - Monthly cost review process

Based on my infrastructure: [describe your cloud setup, current monthly cost, and growth trajectory]

## Tips

Adapted from DuploCloud's DevOps prompts. Cloud costs are the silent killer of startups. Source: duplocloud.com/blog/10-prompts-every-engineer-doing-devops-should-know
