---
title: "OpenClaw: Error Log Analyzer"
slug: openclaw-error-log-analyzer
stage: Build
category: "OpenClaw"
grade: C
score: 63
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-error-log-analyzer
---
# OpenClaw: Error Log Analyzer

Error Log Analyzer Ingest log files, identify unique errors, and provide actionable summaries.

## Prompt

# Error Log Analyzer

Ingest log files, identify unique errors, and provide actionable summaries.

## Input
- Log file(s) or stream of log data

## Processing
- Parse each log entry: extract timestamp, log level (ERROR, WARNING), message
- Group similar error messages, ignoring minor variations (timestamps, request IDs)
- Track per unique error: occurrence count, first seen, last seen

## Analysis
- Identify most frequent errors
- Detect spikes in error rates
- Look for correlations between different errors
- Flag new errors not seen in previous runs

## Output
Summary report with:
- Total error count
- Unique errors sorted by frequency
- Timeline of error occurrences
- Spike detection alerts
- Suggested root causes based on error patterns

## Notifications
Optionally send alerts via Slack or Telegram when:
- New error type appears
- Error rate exceeds threshold
- Critical errors detected

## Tips

Log analysis automation that groups errors, detects spikes, and identifies correlations. From mberman84's developer automation gist.
