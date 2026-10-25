---
title: "OpenClaw: A/B Test Analyzer"
slug: openclaw-a-b-test-analyzer
stage: Build
category: "OpenClaw"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-a-b-test-analyzer
---
# OpenClaw: A/B Test Analyzer

A/B Test Analyzer — OpenClaw Workflow Prompt Trigger Activate when experiment data is shared or when asked to analyze an A/B test.

Variables: PASS/FAIL, result, checked segments, day-over-day trend, was test stopped early?, correction applied?, Experiment Name, Primary metric, value, count, +X.X%, lower, upper, days, Ship / Don't ship / Extend test, 1-2 sentences, Any concerns

## Prompt

# A/B Test Analyzer — OpenClaw Workflow Prompt

## Trigger
Activate when experiment data is shared or when asked to analyze an A/B test.

## Analysis Pipeline

### 1. Validity Checks (Before Results)
- **Sample Ratio Mismatch (SRM):** Chi-square test on control/treatment split. Flag if p < 0.01.
- **Minimum sample size:** Was the test run long enough? Calculate required n for desired power.
- **Novelty/primacy effects:** Check if effect is concentrated in first/last days.
- **Multiple testing correction:** If >1 metric tested, apply Bonferroni or Holm correction.

### 2. Statistical Analysis
- **Point estimate:** Difference in means/proportions
- **Confidence interval:** 95% CI for the effect size
- **P-value:** Two-sided test (and one-sided if directional hypothesis)
- **Effect size:** Cohen's d or relative lift
- **Statistical power:** Given the observed effect, what was the actual power?

### 3. Pitfall Detection
```
⚠️ PITFALL CHECK
[{{PASS/FAIL}}] Sample Ratio Mismatch: {{result}}
[{{PASS/FAIL}}] Simpson's Paradox: {{checked segments}}
[{{PASS/FAIL}}] Novelty Effect: {{day-over-day trend}}
[{{PASS/FAIL}}] Peeking: {{was test stopped early?}}
[{{PASS/FAIL}}] Multiple Comparisons: {{correction applied?}}
```

### 4. Segment Analysis
- Break results by key segments (device, geo, user tenure, etc.)
- Flag segments where treatment effect reverses (Simpson's paradox)
- Identify segments with strongest/weakest effects

### 5. Executive Summary
```
🧪 A/B TEST RESULTS — {{Experiment Name}}

Metric: {{Primary metric}}
Control: {{value}} (n={{count}})
Treatment: {{value}} (n={{count}})
Lift: {{+X.X%}} | 95% CI: [{{lower}}, {{upper}}]
P-value: {{value}} | Power: {{value}}
Duration: {{days}} | Required: {{days}}

RECOMMENDATION: {{Ship / Don't ship / Extend test}}
Reason: {{1-2 sentences}}
Caveats: {{Any concerns}}
```

## Tips

Calculates statistical significance, detects Simpson's paradox, novelty effects, and sample ratio mismatch. From Analytics Vidhya's 20 OpenClaw Prompts.
