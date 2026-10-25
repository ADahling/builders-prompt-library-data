---
title: "Fix Dependent Field Validation in a Dynamic Form"
slug: fix-dependent-field-validation-in-a-dynamic-form
stage: Test
category: "Functional Bugs"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-dependent-field-validation-in-a-dynamic-form
---
# Fix Dependent Field Validation in a Dynamic Form

Correct a React form bug by implementing conditional Yup validation to make the shipping address field required only for physical products.

Variables: project_name, app_type, tech_stack, form_library, CheckoutForm.tsx

## Prompt

You are a developer working on a feature for {{project_name}}, a {{app_type}} application built with {{tech_stack}}. The feature involves a dynamic form where a "Shipping Address" section is only required if the user selects "Physical Product" from a "Product Type" dropdown. The bug is that the shipping address fields are always being treated as required, even when "Digital Product" is selected.

Your task is to fix this conditional validation logic.

**Context:**
- **Framework:** {{tech_stack}}
- **Form Library:** {{form_library}}
- **File:** '/path/to/{{CheckoutForm.tsx}}'

**Relevant Form Logic Snippet:**
```typescript
// Using {{form_library}} for form state and validation

const validationSchema = Yup.object({
  productType: Yup.string().required("Product type is required"),
  // This is the problematic part
  shippingAddress: Yup.string().required("Shipping address is required"),
});

const CheckoutForm = () => {
  const formik = useFormik({
    initialValues: { productType: "digital", shippingAddress: "" },
    validationSchema,
    onSubmit: (values) => {
      console.log(values);
    },
  });

  return (
    <form onSubmit={formik.handleSubmit}>
      <select name="productType" {...formik.getFieldProps("productType")}>
        <option value="digital">Digital Product</option>
        <option value="physical">Physical Product</option>
      </select>
      {/* ... other form fields ... */}
      <input name="shippingAddress" {...formik.getFieldProps("shippingAddress")} />
      {formik.errors.shippingAddress && <div>{formik.errors.shippingAddress}</div>}
    </form>
  );
};
```

**Instructions:**

1.  **Identify the Issue:** Explain why the `shippingAddress` field is always being validated, regardless of the `productType` value.
2.  **Implement Conditional Validation:** Using the features available in the {{form_library}} library (specifically, the `when` conditional validation method), modify the `validationSchema` to make the `shippingAddress` field required only when `productType` is "physical".
3.  **Explain the Solution:** Describe how the `when` method works in this context and why it is the correct approach for handling dependent field validation.

**Output Format:**

- **Root Cause Analysis:** A clear explanation of the validation issue.
- **Corrected `validationSchema`:** The complete, corrected Yup validation schema.
- **Explanation of the Fix:** A detailed description of how the conditional validation works.

## Tips

A good example of conditional validation in a dynamic form, common in e-commerce.
