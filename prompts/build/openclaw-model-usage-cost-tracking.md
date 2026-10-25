---
title: "OpenClaw: Model Usage & Cost Tracking"
slug: openclaw-model-usage-cost-tracking
stage: Build
category: "OpenClaw"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-model-usage-cost-tracking
---
# OpenClaw: Model Usage & Cost Tracking

Set up AI API call logging, token cost estimates, spending reports, and routing suggestions for tracking model usage across workflows.

## Prompt

# Model Usage & Cost Tracking

Log every AI API call and provide cost visibility.

## Logging
Wrap every LLM/AI API call with a logger recording (JSONL format):
```json
{
  "timestamp": "ISO8601",
  "model": "model-name",
  "tokens": { "input": 1500, "output": 800, "total": 2300 },
  "taskType": "crm-ingestion",
  "description": "Classify 25 new email contacts",
  "costEstimate": 0.045,
  "source": "crm-pipeline"
}
```

## Cost Calculation (per 1M tokens, input/output)
- Anthropic: Claude Opus 4.8 ($15/$75), Claude Sonnet 5 ($3/$15), Haiku ($0.80/$4)
- OpenAI: GPT-5 ($30/$60), GPT-5 Turbo ($10/$30), o1 ($15/$60)
- Google: Gemini 3 Pro ($10/$30), Flash ($0.30/$1.20)
- Default unknown: $1/$3

Formula: (inputTokens / 1M) × inputPrice + (outputTokens / 1M) × outputPrice

## Reporting (on demand, with filters)
1. Overall: total calls, tokens, cost
2. By model: sorted by cost descending
3. By task type: sorted by cost descending
4. By day: last 10 days
5. Trend: daily/weekly spending over 30/90 days

## Routing Suggestions
- Flag frontier model usage on simple tasks → suggest downgrade
- Flag workflows >25% of total spend → optimization candidates
- Suggest caching for repeated queries

## Output
Markdown report or web dashboard. Weekly cost summary to chat.

## Tips

Tracks every AI API call with per-model pricing, generates cost reports, and suggests model routing optimizations. From mberman84's extended gist.
