# CSS Introduction

## What is CSS?

CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML. CSS describes how elements should be rendered on screen, on paper, or in other media.

## CSS Syntax

CSS follows a simple syntax structure:

```css
selector {
    property: value;
    property: value;
}
```

**Components:**
- **Selector**: Targets the HTML element(s) to style
- **Property**: The style attribute you want to change
- **Value**: The setting for the property
- **Declaration**: A property-value pair
- **Declaration Block**: All declarations enclosed in curly braces

**Example:**
```css
h1 {
    color: blue;
    font-size: 24px;
}
```

## Basic CSS Properties

### Text Properties
- `color`: Sets text color
- `font-size`: Sets text size
- `font-family`: Sets font type
- `font-weight`: Sets text thickness (bold, normal)
- `text-align`: Aligns text (left, center, right)

### Background Properties
- `background-color`: Sets background color
- `background-image`: Sets background image

### Box Model Properties
- `margin`: Space outside the element
- `padding`: Space inside the element
- `border`: Border around the element
- `width`: Element width
- `height`: Element height

## Types of CSS Application

### 1. Inline CSS
CSS is applied directly to HTML elements using the `style` attribute.

**Syntax:**
```html
<element style="property: value; property: value;">Content</element>
```

**Example:**
```html
<p style="color: red; font-size: 18px;">This is red text</p>
```

**Characteristics:**
- Highest specificity
- Applied to individual elements
- Not recommended for large projects

### 2. Internal CSS
CSS is written within `<style>` tags in the HTML document's `<head>` section.

**Syntax:**
```html
<head>
    <style>
        selector {
            property: value;
        }
    </style>
</head>
```

**Example:**
```html
<head>
    <style>
        p {
            color: blue;
            font-size: 16px;
        }
    </style>
</head>
```

**Characteristics:**
- Applies to the entire HTML document
- Good for single-page styling
- Better than inline for multiple elements

### 3. External CSS
CSS is written in separate `.css` files and linked to HTML documents.

**Two Ways to Apply External CSS:**

#### Method 1: Using `<link>` Tag (Recommended)
**Syntax:**
```html
<head>
    <link rel="stylesheet" href="path/to/stylesheet.css">
</head>
```

**Example:**
```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

#### Method 2: Using `@import` Rule
**Syntax:**
```html
<head>
    <style>
        @import url("path/to/stylesheet.css");
    </style>
</head>
```

**Example:**
```html
<head>
    <style>
        @import url("styles.css");
    </style>
</head>
```

**Characteristics:**
- Most recommended approach
- Reusable across multiple pages
- Better performance and maintainability
- `<link>` method loads faster than `@import`

## Why CSS is Called "Cascading"?

CSS is called "Cascading" because styles "cascade" or flow down from multiple sources and get applied in a specific order of priority. Think of it like a waterfall where water flows from top to bottom.

### How Cascading Works:

1. **Multiple Style Sources**: You can have styles from different places:
   - Browser default styles
   - External CSS files
   - Internal CSS (in `<style>` tags)
   - Inline CSS (in `style` attributes)

2. **Priority Order** (from lowest to highest):
   - Browser defaults
   - External CSS
   - Internal CSS
   - Inline CSS

3. **The Last Rule Wins**: If there are conflicting styles of the same priority, the last one applied wins.

**Example:**
```css
/* External CSS */
p { color: blue; }

/* Internal CSS - This will override external */
p { color: red; }
```

**Result**: Paragraphs will be red because internal CSS has higher priority than external CSS.

### Inheritance:
Some CSS properties are inherited from parent elements to child elements, like a family trait passed down from parents to children.

**Example:**
```css
body { color: green; }
/* All text inside body will be green unless specifically changed */
```

## Benefits of CSS

- Separation of content and presentation
- Reusability across multiple pages
- Easier maintenance and updates
- Better performance through caching
- Responsive design capabilities
- Consistent styling across website