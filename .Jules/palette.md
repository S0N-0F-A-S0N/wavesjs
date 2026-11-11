## 2024-11-11 - Semantic HTML and Screen Reader Support
**Learning:** Legacy webgl experiments often completely lack basic web accessibility (missing lang tags, viewports, structural elements, and semantic roles for visual components). The canvas needs a specific aria-label and role="img" when used for visualization, while purely visual UI overlay layers should be hidden from screen readers.
**Action:** Always start by auditing the root HTML file for structural and foundational accessibility before trying to modify specific UI components in JS.
