# Pseudo Elements

## Pseudo Elements Definition

Pseudo-elements are virtual elements that allow you to style specific parts of an element's content. Unlike pseudo-classes that target elements based on their state, pseudo-elements let you style particular portions of an element, such as the first letter, first line, or insert content before/after an element.

**Syntax:** Pseudo-elements use double colons (::) in CSS3, though single colon (:) is still supported for backward compatibility.

```css
selector::pseudo-element {
    property: value;
}
```

## Types of Pseudo Elements

### 1. ::before

**Definition:** Inserts content before an element's actual content.

**Syntax:**
```css
selector::before {
    content: "text or symbol";
    property: value;
}
```

**Example:**
```css
h2::before {
    content: "★ ";
    color: gold;
    font-weight: bold;
}

.quote::before {
    content: """;
    font-size: 2em;
    color: #666;
}
```

### 2. ::after

**Definition:** Inserts content after an element's actual content.

**Syntax:**
```css
selector::after {
    content: "text or symbol";
    property: value;
}
```

**Example:**
```css
.price::after {
    content: " USD";
    color: #666;
    font-size: 0.8em;
}

a[href^="http"]::after {
    content: " ↗";
    color: blue;
}
```

### 3. ::first-letter

**Definition:** Styles the first letter of the first line of a block-level element.

**Syntax:**
```css
selector::first-letter {
    property: value;
}
```

**Example:**
```css
p::first-letter {
    font-size: 3em;
    font-weight: bold;
    color: #333;
    float: left;
    margin-right: 5px;
}
```

### 4. ::first-line

**Definition:** Styles the first line of a block-level element.

**Syntax:**
```css
selector::first-line {
    property: value;
}
```

**Example:**
```css
p::first-line {
    font-weight: bold;
    color: #007bff;
    text-transform: uppercase;
}
```

### 5. ::selection

**Definition:** Styles the portion of text selected by the user.

**Syntax:**
```css
selector::selection {
    property: value;
}
```

**Example:**
```css
::selection {
    background-color: #007bff;
    color: white;
}

p::selection {
    background-color: yellow;
    color: black;
}
```

## Key Points

1. **Content Property:** Required for ::before and ::after pseudo-elements
2. **Display Property:** ::before and ::after are inline by default
3. **Positioning:** Pseudo-elements can be positioned like regular elements
4. **Inheritance:** Pseudo-elements inherit from their parent element
5. **Browser Support:** Well supported in modern browsers

## Best Practices

1. Always include the `content` property for ::before and ::after
2. Use pseudo-elements for decorative content, not essential information
3. Consider accessibility when adding content via pseudo-elements
4. Use ::selection to enhance user experience
5. Combine with transitions for smooth effects