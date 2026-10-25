---
title: "OpenClaw: Earnings Report Monitor"
slug: openclaw-earnings-report-monitor
stage: Build
category: "OpenClaw"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-earnings-report-monitor
---
# OpenClaw: Earnings Report Monitor

Set up watchlist earnings previews and post-release alerts comparing results with expectations, plus guidance highlights and stock reactions.

Variables: date, TICKER, Company Name, quarter, year, actual, expected, beat/miss by X%, beat/miss, 📈 Strong Beat / ✅ In-Line / 📉 Miss, Key metric 1 and its significance, Key metric 2, Notable guidance change, stock movement, 1-2 sentence narrative summary

## Prompt

# Earnings Report Monitor — OpenClaw Automation

## Pipeline
### 1. Sunday Preview (9:00 AM)
Scan watchlist stocks (configured in USER.md) for upcoming earnings:

```
📈 EARNINGS PREVIEW — Week of {{date}}

Monday: No earnings on watchlist
Tuesday: AAPL (Apple) — After market close
  - Consensus EPS: $2.35 | Revenue: $95.2B
  - Key metrics to watch: iPhone revenue, Services growth, China sales
  - Last quarter: Beat by 4%, stock +3.2%

Wednesday: MSFT (Microsoft) — After market close
  - Consensus EPS: $3.12 | Revenue: $65.8B
  - Key metrics to watch: Azure growth rate, AI revenue, Copilot adoption
```

### 2. Dynamic Post-Earnings Alerts
Create one-time cron jobs timed to 30 minutes after each earnings release:

```
📊 EARNINGS ALERT — {{TICKER}}

{{Company Name}} Q{{quarter}} {{year}}

EPS: ${{actual}} vs ${{expected}} ({{beat/miss by X%}})
Revenue: ${{actual}} vs ${{expected}} ({{beat/miss}})

VERDICT: {{📈 Strong Beat / ✅ In-Line / 📉 Miss}}

Key Highlights:
- {{Key metric 1 and its significance}}
- {{Key metric 2}}
- {{Notable guidance change}}

After-Hours: {{stock movement}}

Takeaway: {{1-2 sentence narrative summary}}
```

### 3. Self-Cleanup
- Post-earnings cron jobs auto-delete after execution
- Weekly summary of all earnings results added to memory
- Track prediction accuracy over time

## Tips

Sunday preview of upcoming earnings, dynamic post-earnings alerts with auto-cleanup. From mberman84's gist.
