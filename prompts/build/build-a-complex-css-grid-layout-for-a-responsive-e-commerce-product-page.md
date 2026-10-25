---
title: "Build a Complex CSS Grid Layout for a Responsive E-commerce Product Page"
slug: build-a-complex-css-grid-layout-for-a-responsive-e-commerce-product-page
stage: Build
category: "Frontend & Styling"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-complex-css-grid-layout-for-a-responsive-e-commerce-product-page
---
# Build a Complex CSS Grid Layout for a Responsive E-commerce Product Page

Generate a responsive, multi-column e-commerce product layout using CSS Grid and SCSS with grid-template-areas for fluid breakpoint adaptation.

Variables: website_name

## Prompt

I am designing a product detail page for an e-commerce website, {{website_name}}, and I need a sophisticated, responsive layout using CSS Grid. The page has several sections: a product image gallery, product title and description, price and add-to-cart button, customer reviews, and related products.

Create the HTML structure and the corresponding CSS (using SCSS for better organization) to implement the following layout:
-   **Desktop (1200px and above):** A three-column layout. The first column contains the image gallery. The second column displays the product title, description, and reviews. The third column shows the price, add-to-cart options, and related products.
-   **Tablet (768px to 1199px):** A two-column layout. The image gallery takes the first column, and all other content (title, description, price, reviews, etc.) flows into the second column.
-   **Mobile (below 768px):** A single-column layout where all sections stack vertically in a logical order: image gallery, title, price, description, reviews, and finally related products.

Your CSS Grid implementation should:
1.  Use 'grid-template-areas' for clarity and easy maintenance.
2.  Be fully responsive and adapt to the specified breakpoints without using a separate mobile-first or desktop-first approach. The grid definition should adapt fluidly.
3.  Ensure proper alignment and spacing between grid items using 'gap', 'align-items', and 'justify-content'.
4.  The solution should be pure HTML and SCSS. Do not use any JavaScript for layout manipulation.

Provide the complete HTML and SCSS code. Add comments to the SCSS to explain the grid setup for each breakpoint.
