---
title: "Cloning a Data Visualization Chart"
slug: cloning-a-data-visualization-chart
stage: Build
category: "Website Cloning"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cloning-a-data-visualization-chart
---
# Cloning a Data Visualization Chart

Replicate specific interactive web charts by extracting data and generating functional code using libraries like D3.js, Chart.js, or Highcharts.

Variables: chart_page_url

## Prompt

You are a data visualization enthusiast. Your task is to clone a single data visualization chart (e.g., a bar chart, a line chart, a pie chart) from a data-rich website or dashboard. The chart should be interactive, with tooltips that appear on hover.

Context:
- The chart to clone is on the page {{chart_page_url}}.
- You must use a charting library like Chart.js, D3.js, or Highcharts to create the chart.
- You will need to extract the data from the original chart or use a sample dataset to populate your cloned chart.

Provide:
1. The code for the interactive data visualization chart.
2. The data you used to generate the chart, in JSON format.

If you cannot open {{chart_page_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

A great way to learn how to work with data visualization libraries and create interactive charts.
