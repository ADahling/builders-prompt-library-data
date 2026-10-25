---
title: "Create an E2E Test for a Multi-Step Wizard Form"
slug: create-an-e2e-test-for-a-multi-step-wizard-form
stage: Test
category: "Testing & QA"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-e2e-test-for-a-multi-step-wizard-form
---
# Create an E2E Test for a Multi-Step Wizard Form

Get a modular E2E script for a wizard form that fills each step, checks Next and Back navigation, submits, and verifies processed data.

Variables: wizard_purpose, e2e_framework, wizard_steps

## Prompt

Our application features a multi-step wizard for `{{wizard_purpose}}`. I need an end-to-end test that simulates a user going through the entire wizard, filling out each step, and successfully submitting the form.

**Instructions:**
1.  **Testing Framework:** Use `{{e2e_framework}}`.
2.  **Wizard Steps:** The wizard has the following steps: `{{wizard_steps}}`.
3.  **Test Implementation:**
    *   The test should navigate to the first step of the wizard.
    *   For each step, it should fill in the required fields with valid data.
    *   It should click the "Next" button to proceed to the next step and the "Back" button to test navigation.
    *   On the final step, it should submit the form.
    *   After submission, it should verify that the user sees a success message and that the data was correctly processed (e.g., by checking the UI for the results or making an API call to verify the backend state).
4.  **Output Format:** Provide the complete E2E test script. The code should be modular, with helper functions for filling out each step of the wizard to improve readability and maintainability.
