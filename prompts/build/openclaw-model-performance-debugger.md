---
title: "OpenClaw: Model Performance Debugger"
slug: openclaw-model-performance-debugger
stage: Build
category: "OpenClaw"
grade: A
score: 83
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-model-performance-debugger
---
# OpenClaw: Model Performance Debugger

Model Performance Debugger — OpenClaw Workflow Prompt Trigger Activate when model metrics are pasted or when asked to debug model performance.

Variables: metrics, underfitting / overfitting / class imbalance / data quality, Specific hyperparameter change with expected impact, Data augmentation strategy, Feature engineering suggestion, Architecture change, Data collection strategy, Ensemble approach

## Prompt

# Model Performance Debugger — OpenClaw Workflow Prompt

## Trigger
Activate when model metrics are pasted or when asked to debug model performance.

## Diagnostic Framework

### 1. Confusion Matrix Analysis
- Per-class precision, recall, F1
- Most confused class pairs
- False positive vs. false negative cost analysis
- Threshold optimization recommendations

### 2. Precision/Recall Tradeoffs
- Current operating point on PR curve
- Recommended thresholds for different business objectives:
  - Minimize false positives (fraud detection, spam)
  - Minimize false negatives (medical diagnosis, security)
  - Balance both (general classification)

### 3. Calibration Analysis
- Reliability diagram assessment
- Brier score
- Expected calibration error (ECE)
- Recommendation: Does this model need Platt scaling or isotonic regression?

### 4. Feature Importance
- Rank features by importance (permutation-based)
- Identify features that hurt performance (negative importance)
- Feature redundancy detection (highly correlated feature pairs)
- Minimal feature set that achieves 95% of full performance

### 5. Error Analysis
- Systematic error patterns (which subgroups fail?)
- Hardest examples (highest loss samples)
- Data quality issues surfaced by errors
- Domain shift indicators

## Recommendations
```
📊 MODEL DIAGNOSIS

Current performance: {{metrics}}
Primary issue: {{underfitting / overfitting / class imbalance / data quality}}

Quick wins:
1. {{Specific hyperparameter change with expected impact}}
2. {{Data augmentation strategy}}
3. {{Feature engineering suggestion}}

Larger improvements:
1. {{Architecture change}}
2. {{Data collection strategy}}
3. {{Ensemble approach}}
```

## Tips

Analyzes model metrics, suggests hyperparameter tuning, recommends data augmentation strategies. From Analytics Vidhya's 20 OpenClaw Prompts.
