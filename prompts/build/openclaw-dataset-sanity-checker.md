---
title: "OpenClaw: Dataset Sanity Checker"
slug: openclaw-dataset-sanity-checker
stage: Build
category: "OpenClaw"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-dataset-sanity-checker
---
# OpenClaw: Dataset Sanity Checker

Dataset Sanity Checker — OpenClaw Workflow Prompt Trigger Activate on CSV file upload or when asked to analyze a dataset.

Variables: count, MB, numeric, categorical, datetime, text

## Prompt

# Dataset Sanity Checker — OpenClaw Workflow Prompt

## Trigger
Activate on CSV file upload or when asked to analyze a dataset.

## Automated Analysis Pipeline

### 1. Schema Overview
```
📊 DATASET PROFILE
Rows: {{count}} | Columns: {{count}} | Size: {{MB}}
Dtypes: {{numeric}}/{{categorical}}/{{datetime}}/{{text}}
Memory usage: {{MB}}
```

### 2. Missing Data Analysis
- Percentage missing per column (flag >5%)
- Missing data patterns: MCAR / MAR / MNAR assessment
- Columns to consider dropping (>50% missing)
- Recommended imputation strategies per column

### 3. Cardinality & Distribution
- Categorical columns: unique values, top-5 frequencies, rare categories
- Numeric columns: mean, median, std, min, max, skewness, kurtosis
- Date columns: range, gaps, frequency
- Potential ID columns (unique per row)

### 4. Outlier Detection
- IQR method: flag values beyond 1.5× IQR
- Z-score method: flag values beyond 3 standard deviations
- Visual indicators for extreme values

### 5. Target Variable Analysis (if specified)
- Class balance assessment
- Target correlation with features
- Target leakage detection — features that perfectly predict target

### 6. Data Quality Flags
```
🚩 QUALITY FLAGS
[CRITICAL] Target leakage: 'account_status' perfectly predicts churn
[HIGH] 'email' column has 12% duplicates — possible data collection issue
[MEDIUM] 'age' has 3 values of 999 — likely sentinel for missing
[LOW] 'signup_date' has 2 records from 1970 — epoch default?
```

### 7. Recommendations
- Preprocessing steps (ordered by priority)
- Feature engineering opportunities
- 3 recommended baseline models with justification
- Train/test split strategy (time-based? stratified?)

## Tips

Triggers on CSV upload. Generates comprehensive data quality report with leakage detection and baseline model recommendations. From Analytics Vidhya's 20 OpenClaw Prompts.
