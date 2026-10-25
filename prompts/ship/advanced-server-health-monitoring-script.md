---
title: "Advanced Server Health Monitoring Script"
slug: advanced-server-health-monitoring-script
stage: Ship
category: "Monitoring & Observability"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-server-health-monitoring-script
---
# Advanced Server Health Monitoring Script

Get a cron-ready server monitoring script with CPU, disk, network, and memory checks, threshold alerts, JSON output, and error handling.

Variables: project_name, programming_language, server_name, cpu_load, disk_usage, network_inbound, network_outbound, memory_utilization, alert_message_if_any

## Prompt

Develop a script to monitor the health of servers in your infrastructure for the {{project_name}} initiative. The script should be capable of checking CPU load, disk usage, network I/O, and memory utilization on each server. It should trigger alerts when any metric exceeds the specified threshold limits. Write the script in {{programming_language}} and ensure it runs efficiently on a cron job. Your script should output in the following JSON format:

{
  "server_name": "{{server_name}}",
  "metrics": {
    "cpu_load": {{cpu_load}},
    "disk_usage": {{disk_usage}},
    "network_io": {
      "inbound": {{network_inbound}},
      "outbound": {{network_outbound}}
    },
    "memory_utilization": {{memory_utilization}}
  },
  "alert": "{{alert_message_if_any}}"
}

Ensure the script is well-documented and includes error handling mechanisms.

## Tips

Designed for advanced users needing to automate server health checks.
