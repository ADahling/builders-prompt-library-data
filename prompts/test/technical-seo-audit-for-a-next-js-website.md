---
title: "Technical SEO Audit for a Next.js Website"
slug: technical-seo-audit-for-a-next-js-website
stage: Test
category: "Quality Audits"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/technical-seo-audit-for-a-next-js-website
---
# Technical SEO Audit for a Next.js Website

Conduct a comprehensive technical SEO audit for Next.js sites to optimize SSR/SSG performance, indexability, and organic search rankings.

Variables: project_name, project_description, tech_stack

## Prompt

As an SEO specialist, I need you to perform a comprehensive technical SEO audit for our website, `{{project_name}}`, which is built with Next.js. The website is a {{project_description}} and our goal is to improve our organic search rankings and drive more traffic to the site. The website is built on {{tech_stack}}.

Your audit should cover all aspects of technical SEO, with a specific focus on the nuances of Next.js applications, including:

1.  **Crawlability and Indexability:**
    *   Analyze the `robots.txt` file and XML sitemap for any errors or optimization opportunities.
    *   Check for any crawl errors in Google Search Console.
    *   Ensure that all important pages are being indexed by Google, paying special attention to server-side rendered (SSR) and statically generated (SSG) pages.

2.  **On-Page SEO:**
    *   Analyze the use of title tags, meta descriptions, and header tags, ensuring they are being rendered correctly on the server.
    *   Check for duplicate content issues.
    *   Evaluate the internal linking structure and identify opportunities for improvement.
    *   Assess the mobile-friendliness of the website.

3.  **Site Speed and Performance:**
    *   Analyze the website's loading speed using tools like Google PageSpeed Insights, paying close attention to Next.js specific metrics like Time to First Byte (TTFB) for SSR pages.
    *   Identify any factors that are slowing down the website and provide recommendations for improvement, such as optimizing `getStaticProps` and `getServerSideProps`.

4.  **Structured Data:**
    *   Check for the implementation of structured data (e.g., Schema.org) and identify any errors or opportunities for improvement.

5.  **International SEO:**
    *   If applicable, review the implementation of hreflang tags for international targeting, ensuring they are correctly implemented in the Next.js routing.

**Output Format:**

Please provide a technical SEO audit report in a Markdown file with the following structure:

*   **Executive Summary:** A high-level overview of the website's technical SEO health and a summary of the most critical issues found.
*   **Audit Findings:** A detailed list of all identified issues, categorized by the areas mentioned above. For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **Severity:** (High, Medium, Low)
    *   **Description:** A clear explanation of the issue and its impact on SEO.
    *   **Recommendation:** Specific and actionable steps to fix the issue.
*   **SEO Action Plan:** A prioritized list of recommendations to improve the website's technical SEO.
