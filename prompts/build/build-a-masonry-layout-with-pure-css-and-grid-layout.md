---
title: "Build a Masonry Layout with Pure CSS and Grid Layout"
slug: build-a-masonry-layout-with-pure-css-and-grid-layout
stage: Build
category: "Frontend & Styling"
grade: B
score: 75
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-masonry-layout-with-pure-css-and-grid-layout
---
# Build a Masonry Layout with Pure CSS and Grid Layout

Get HTML and CSS for a responsive Grid-based masonry image gallery, with commented layout techniques and an explanation of pure CSS limitations.

Variables: website_name

## Prompt

For our image gallery on {{website_name}}, we want to implement a Masonry-style layout where images of varying heights are arranged in columns without large gaps. We want to achieve this using modern CSS, specifically CSS Grid Layout, to avoid the performance overhead of JavaScript-based solutions.

Create the HTML and CSS to build a responsive, multi-column Masonry layout.

The CSS implementation should:
1.  Use CSS Grid to create the column structure.
2.  The number of columns should be responsive, for example, 4 columns on large screens, 3 on medium, and 2 on small screens.
3.  The key to the Masonry effect with Grid is to make items span multiple rows based on their content height. You will need to calculate the appropriate 'grid-row-end' value.
4.  This is a challenging task with pure CSS. You may need to use a combination of grid properties and potentially some clever selectors or properties to make it work without JavaScript to measure element heights.
5.  The solution must be robust enough to handle a variable number of items with different aspect ratios.

Provide the complete HTML and CSS for the Masonry layout. The HTML should contain a list of items (e.g., images) to be laid out. The CSS should be well-commented to explain the technique used to create the Masonry effect. If a pure CSS solution is too limited, briefly explain the limitations and suggest a minimal JavaScript enhancement.
