# Child Selectors

## Advanced Selectors Introduction

Advanced CSS selectors provide powerful ways to target specific elements based on their relationships with other elements in the HTML document. These selectors help create more precise and flexible styling rules.

## Combinators Overview

CSS combinators define the relationship between selectors:

- **Space ( )** - Descendant combinator
- **>** - Child combinator  
- **+** - Adjacent sibling combinator
- **~** - General sibling combinator

## Child Selectors Definition

Child selectors target elements that are direct children of another element. Unlike descendant selectors that target all nested elements, child selectors only affect immediate children.

**Key Difference:**
- **Descendant (space)**: Targets all nested elements at any level
- **Child (>)**: Targets only direct children (one level down)

## Types of Child Selectors

### 1. Direct Child Selector (>)

**Definition:** Selects elements that are direct children of a specified parent.

**Syntax:**
```css
parent > child {
    property: value;
}
```

**Example:**
```css
ul > li {
    color: blue;
}

.container > p {
    font-weight: bold;
}
```

**Use Case:** Style only immediate children, not deeper nested elements.

### 2. First Child (:first-child)

**Definition:** Selects the first child element of its parent.

**Syntax:**
```css
selector:first-child {
    property: value;
}
```

**Example:**
```css
li:first-child {
    color: red;
}

p:first-child {
    margin-top: 0;
}
```

### 3. Last Child (:last-child)

**Definition:** Selects the last child element of its parent.

**Syntax:**
```css
selector:last-child {
    property: value;
}
```

**Example:**
```css
li:last-child {
    border-bottom: none;
}

.item:last-child {
    margin-bottom: 0;
}
```

### 4. Nth Child (:nth-child())

**Definition:** Selects elements based on their position among siblings.

**Syntax:**
```css
selector:nth-child(n) {
    property: value;
}
```

**Examples:**
```css
/* Select 3rd child */
li:nth-child(3) {
    color: green;
}

/* Select even children */
tr:nth-child(even) {
    background-color: #f2f2f2;
}

/* Select odd children */
li:nth-child(odd) {
    background-color: lightblue;
}
```

### 5. Only Child (:only-child)

**Definition:** Selects elements that are the only child of their parent.

**Syntax:**
```css
selector:only-child {
    property: value;
}
```

**Example:**
```css
p:only-child {
    text-align: center;
    font-weight: bold;
}
```

## Best Practices

1. Use child selectors when you need precise control over styling
2. Combine with class selectors for better specificity
3. Consider performance - child selectors are generally fast
4. Use :first-child and :last-child to remove margins/borders
5. Use :nth-child() for alternating row colors in tables