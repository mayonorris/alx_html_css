# CSS Basics — ALX Front-End

Build a solid foundation in **CSS** by styling a small, standards-compliant website (no frameworks). You’ll practice selectors, classes, the cascade, **specificity**, and the **box model**, while keeping everything W3C-valid.

---

## Learning Objectives

By the end, you can explain and demonstrate:

- **What CSS is** and how browsers load/apply it.
- **How to add style** to elements (external stylesheets, inline vs internal).
- **Selectors & classes** (element, class, ID, attribute, pseudo-classes/elements).
- **CSS specificity** (and how to compute it).
- **Box properties** (content, padding, border, margin; width/height; box-sizing).
- **Validation & quality** (W3C HTML/CSS validators, accessible markup).

---

## Project Structure

```text
alx_html_css/
└─ css_basic/
├─ README.md
├─ base.css # Global reset/base tokens (variables, normalize, typography)
├─ styles.css # Page-level, component styles (layout, utilities)
├─ index.html # Home page (links both CSS files)
└─ tweets.html # Tweets page (links both CSS files)
```

**Rule of thumb**
- **`base.css`**: low-specificity, foundational styles (normalize, variables, defaults).
- **`styles.css`**: actual design (layout, components, utilities). Load **after** `base.css`.

---


## Getting Started

1. Open the `css_basic` folder in VS Code.
2. Ensure both HTML files link the CSS in this order:
   ```html
   <link rel="stylesheet" href="base.css">
   <link rel="stylesheet" href="styles.css">


