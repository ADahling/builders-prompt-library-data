---
title: "Clone Quality Assurance & Pixel-Perfect Audit"
slug: clone-quality-assurance-pixel-perfect-audit
stage: Build
category: "Website Cloning"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/clone-quality-assurance-pixel-perfect-audit
---
# Clone Quality Assurance & Pixel-Perfect Audit

Conduct a detailed visual and functional audit to ensure pixel-perfect fidelity and parity between an original website and its clone.

Variables: original_url, cloned_url

## Prompt

You are a senior QA engineer specializing in visual regression testing and pixel-perfect web reproduction. Perform a comprehensive quality audit comparing the cloned site against the original.

Original URL: {{original_url}}
Cloned URL: {{cloned_url}}

## Visual Regression Audit
1. **Pixel Comparison**: Compare screenshots at 320px, 768px, 1024px, 1440px, and 1920px breakpoints. Document every visual deviation with coordinates and severity.
2. **Typography Audit**: Compare font rendering, sizes, weights, line-heights, and letter-spacing at every breakpoint. Flag any mismatches.
3. **Color Accuracy**: Compare every color value (backgrounds, text, borders, shadows) against the original. Use a color diff tool to measure Delta-E values.
4. **Spacing Verification**: Compare padding, margins, and gaps for every component. Flag deviations greater than 2px.
5. **Component Fidelity**: For each component (nav, hero, cards, forms, footer), rate the reproduction accuracy on a 1-10 scale.

## Functional Parity Audit
1. **Navigation**: Test every link, menu, dropdown, and breadcrumb. Verify identical behavior.
2. **Forms**: Test every form with valid and invalid inputs. Compare validation messages and error states.
3. **Interactions**: Test every hover, click, scroll, and keyboard interaction. Compare timing and behavior.
4. **Responsive Behavior**: Test resize behavior between breakpoints. Verify identical layout shifts.
5. **Performance**: Compare Lighthouse scores (Performance, Accessibility, Best Practices, SEO) between original and clone.

## Cross-Browser Verification
Test in Chrome, Firefox, Safari, and Edge. Document any browser-specific rendering differences between original and clone.

## Output Format
Produce a detailed audit report with:
- Overall fidelity score (percentage)
- Categorized issues (Critical, Major, Minor, Cosmetic)
- Screenshot comparisons for each issue
- Specific CSS/HTML fix for each deviation
- Priority-ordered remediation plan

If you cannot open {{original_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

Final QA step for website cloning. Produces a comprehensive pixel-perfect audit with specific fixes for every deviation.
