---
title: "Fix Missing Loading State Indicator During Data Fetch"
slug: fix-missing-loading-state-indicator-during-data-fetch
stage: Test
category: "Functional Bugs"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-missing-loading-state-indicator-during-data-fetch
---
# Fix Missing Loading State Indicator During Data Fetch

Implement a React loading state to provide visual feedback and prevent a blank screen while product data is being fetched from the API.

Variables: project_name, tech_stack, ProductList.js

## Prompt

You are a developer working on a {{project_name}} e-commerce site. The product listing page fetches a list of products from an API. On slow network connections, the page appears blank for several seconds before the products are displayed, which makes the application feel unresponsive. There is no loading indicator.

Your task is to add a loading state to the component to provide immediate feedback to the user while the data is being fetched.

**Context:**
- **Framework:** {{tech_stack}}
- **File:** '/path/to/{{ProductList.js}}'

**Component Without Loading State:**

```javascript
const ProductList = () => {
  const [products, setProducts] = useState([]);

  useEffect(() => {
    axios.get("/api/products").then(response => {
      setProducts(response.data);
    });
  }, []);

  return (
    <div class="product-grid">
      {products.map(product => <ProductCard key={product.id} product={product} />)}
    </div>
  );
};
```

**Instructions:**

1.  **Explain the UX Problem:** Describe why the absence of a loading indicator is a bad user experience.
2.  **Introduce a Loading State Variable:** Add a new state variable, for example `isLoading

## Tips

Essential for good UX, this prompt teaches the most basic pattern for handling loading states.
