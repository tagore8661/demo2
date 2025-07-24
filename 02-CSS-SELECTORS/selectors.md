# CSS Selectors

## What are CSS Selectors?

CSS selectors are patterns used to select and target HTML elements that you want to style. They act as a bridge between your HTML content and CSS styles, allowing you to specify exactly which elements should receive particular styling rules.

Think of selectors as a way to "point" to specific elements on your webpage and say "apply these styles to these elements."

## Types of CSS Selectors

CSS selectors are divided into two main categories: **Basic Selectors** and **Advanced Selectors**.

---

## Basic Selectors

### 1. Universal Selector (*)

**Definition:** Selects all elements on the page.

**Syntax:**
```css
* {
    property: value;
}
```

**Example:**
```css
* {
    margin: 0;
    padding: 0;
}
```

**Use Case:** Often used to reset default browser styles for all elements.

---

### 2. Element Selector (Type Selector)

**Definition:** Selects all elements of a specific HTML tag type.

**Syntax:**
```css
tagname {
    property: value;
}
```

**Example:**
```css
p {
    color: blue;
    font-size: 16px;
}

h1 {
    color: red;
    text-align: center;
}
```

**Use Case:** Apply styles to all instances of a particular HTML element.

---

### 3. Group Selector

**Definition:** Selects multiple elements and applies the same styles to all of them.

**Syntax:**
```css
selector1, selector2, selector3 {
    property: value;
}
```

**Example:**
```css
h1, h2, h3 {
    color: navy;
    font-family: Arial, sans-serif;
}

p, div, span {
    line-height: 1.5;
}
```

**Use Case:** Avoid repeating the same styles for multiple elements.

---

### 4. Class Selector (.)

**Definition:** Selects elements that have a specific class attribute.

**Syntax:**
```css
.classname {
    property: value;
}
```

**HTML Usage:**
```html
<element class="classname">Content</element>
```

**Example:**
```css
.highlight {
    background-color: yellow;
    padding: 10px;
}

.text-center {
    text-align: center;
}
```

**Use Case:** Style multiple elements that share the same styling purpose. Classes are reusable.

---

### 5. ID Selector (#)

**Definition:** Selects a single element with a specific ID attribute.

**Syntax:**
```css
#idname {
    property: value;
}
```

**HTML Usage:**
```html
<element id="idname">Content</element>
```

**Example:**
```css
#header {
    background-color: #333;
    color: white;
    height: 80px;
}

#main-content {
    width: 80%;
    margin: 0 auto;
}
```

**Use Case:** Style a unique element that appears only once on the page. IDs should be unique.

---

## Advanced Selectors

### 1. Descendant Selector (Space)

**Definition:** Selects elements that are descendants (nested inside) of another element.

**Syntax:**
```css
parent descendant {
    property: value;
}
```

**Example:**
```css
div p {
    color: green;
}

.container h2 {
    margin-bottom: 20px;
}
```

**Use Case:** Style elements only when they appear inside specific parent elements.

---

### 2. Child Selector (>)

**Definition:** Selects elements that are direct children of another element.

**Syntax:**
```css
parent > child {
    property: value;
}
```

**Example:**
```css
ul > li {
    list-style-type: square;
}

.menu > a {
    text-decoration: none;
}
```

**Use Case:** Style only direct children, not deeper nested elements.

---

### 3. Adjacent Sibling Selector (+)

**Definition:** Selects an element that immediately follows another element.

**Syntax:**
```css
element1 + element2 {
    property: value;
}
```

**Example:**
```css
h1 + p {
    font-weight: bold;
}

.button + .button {
    margin-left: 10px;
}
```

**Use Case:** Style elements that come right after specific elements.

---

### 4. Attribute Selector ([])

**Definition:** Selects elements based on their attributes or attribute values.

**Syntax:**
```css
[attribute] {
    property: value;
}

[attribute="value"] {
    property: value;
}
```

**Example:**
```css
[type="text"] {
    border: 1px solid #ccc;
    padding: 5px;
}

[href^="https"] {
    color: green;
}
```

**Use Case:** Style elements based on their attributes, useful for forms and links.

---

### 5. Pseudo-class Selectors (:)

**Definition:** Selects elements based on their state or position.

**Common Pseudo-classes:**
- `:hover` - When mouse hovers over element
- `:active` - When element is being clicked
- `:focus` - When element has focus
- `:first-child` - First child element
- `:last-child` - Last child element

**Syntax:**
```css
selector:pseudo-class {
    property: value;
}
```

**Example:**
```css
a:hover {
    color: red;
    text-decoration: underline;
}

button:active {
    background-color: #333;
}

li:first-child {
    font-weight: bold;
}
```

**Use Case:** Add interactive effects and style elements based on their position or state.

---

## Selector Specificity

CSS selectors have different levels of specificity (priority):

1. **Inline styles** (highest priority)
2. **IDs** (#id)
3. **Classes** (.class), attributes, and pseudo-classes
4. **Elements** (tagname)
5. **Universal selector** (*) (lowest priority)

**Example:**
```css
/* Lower specificity */
p { color: blue; }

/* Higher specificity - this will win */
.highlight { color: red; }

/* Highest specificity - this will win */
#special { color: green; }
```

## Best Practices

1. **Use classes** for reusable styles
2. **Use IDs** for unique elements only
3. **Keep specificity low** for easier maintenance
4. **Use meaningful names** for classes and IDs
5. **Group related selectors** to reduce code repetition
6. **Avoid over-nesting** selectors for better performance