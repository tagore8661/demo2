# Pseudo Classes

## Pseudo Classes Definition

Pseudo-classes are keywords added to selectors that specify a special state or position of an element. They allow you to style elements based on their relationship to the document tree, their position among siblings, or their current state.

**Syntax:** Pseudo-classes are preceded by a colon (:)

```css
selector:pseudo-class {
    property: value;
}
```

## Types of Pseudo Classes

### Structural Pseudo Classes

These pseudo-classes select elements based on their position in the document structure.

### 1. :first-child

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
    font-weight: bold;
    color: red;
}

p:first-child {
    margin-top: 0;
}
```

### 2. :last-child

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

### 3. :nth-child(n)

**Definition:** Selects elements based on their position among siblings.

**Syntax:**
```css
selector:nth-child(n) {
    property: value;
}
```

**Examples:**
```css
/* Select specific position */
li:nth-child(3) {
    color: blue;
}

/* Select even elements */
tr:nth-child(even) {
    background-color: #f2f2f2;
}

/* Select odd elements */
li:nth-child(odd) {
    background-color: lightblue;
}
```

### 4. :only-child

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

### 5. :first-of-type

**Definition:** Selects the first element of its type among siblings.

**Syntax:**
```css
selector:first-of-type {
    property: value;
}
```

**Example:**
```css
h2:first-of-type {
    color: navy;
    font-size: 24px;
}

img:first-of-type {
    border: 2px solid red;
}
```

### 6. :last-of-type

**Definition:** Selects the last element of its type among siblings.

**Syntax:**
```css
selector:last-of-type {
    property: value;
}
```

**Example:**
```css
p:last-of-type {
    margin-bottom: 0;
}

h3:last-of-type {
    border-bottom: 1px solid #ccc;
}
```

### 7. :nth-of-type(n)

**Definition:** Selects elements based on their position among siblings of the same type.

**Syntax:**
```css
selector:nth-of-type(n) {
    property: value;
}
```

**Example:**
```css
/* Select every 2nd paragraph */
p:nth-of-type(2n) {
    background-color: #f9f9f9;
}

/* Select 3rd heading */
h2:nth-of-type(3) {
    color: green;
}
```

### 8. :only-of-type

**Definition:** Selects elements that are the only element of their type among siblings.

**Syntax:**
```css
selector:only-of-type {
    property: value;
}
```

**Example:**
```css
img:only-of-type {
    display: block;
    margin: 0 auto;
}

h1:only-of-type {
    text-align: center;
}
```

## Key Differences

| Pseudo-class | Considers | Example |
|--------------|-----------|---------|
| :first-child | All siblings | First element regardless of type |
| :first-of-type | Same type siblings | First `<p>` among paragraphs |
| :nth-child(2) | All siblings | 2nd element regardless of type |
| :nth-of-type(2) | Same type siblings | 2nd `<p>` among paragraphs |

## Best Practices

1. Use structural pseudo-classes for consistent spacing
2. Combine with element selectors for specificity
3. Use :nth-child() for alternating styles
4. Consider :first-of-type vs :first-child based on your needs
5. Test thoroughly with different HTML structures