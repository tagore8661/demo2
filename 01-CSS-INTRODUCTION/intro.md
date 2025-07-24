# CSS Introduction

## What is CSS?

CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML. CSS describes how elements should be rendered on screen, on paper, or in other media.

## Types of CSS Application

There are three main ways to apply CSS to HTML documents:

### 1. Inline CSS
- CSS is applied directly to HTML elements using the `style` attribute
- Highest specificity but not recommended for large projects
- Example: `<p style="color: red;">Text</p>`

### 2. Internal CSS
- CSS is written within `<style>` tags in the HTML document's `<head>` section
- Applies only to the current HTML document
- Good for single-page styling

### 3. External CSS
- CSS is written in separate `.css` files and linked to HTML documents
- Most recommended approach for maintainability and reusability
- Linked using `<link>` tag in the HTML `<head>` section

## Benefits of CSS

- Separation of content and presentation
- Reusability across multiple pages
- Easier maintenance and updates
- Better performance through caching
- Responsive design capabilities