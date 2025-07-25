# Attribute Selectors

## Attribute Selectors Definition

Attribute selectors target HTML elements based on their attributes or attribute values. They provide a powerful way to style elements without relying on classes or IDs, making CSS more flexible and dynamic.

## Attribute Combinators

CSS attribute selectors use different combinators to match attribute values:

- **=** - Exact match
- **^=** - Starts with
- **$=** - Ends with
- ***=** - Contains
- **~=** - Contains word
- **|=** - Starts with (language codes)

## Types of Attribute Selectors

### 1. Attribute Exists [attribute]

**Definition:** Selects elements that have a specific attribute, regardless of its value.

**Syntax:**
```css
[attribute] {
    property: value;
}
```

**Example:**
```css
[title] {
    border-bottom: 1px dotted;
}

[disabled] {
    opacity: 0.5;
}
```

### 2. Exact Match [attribute="value"]

**Definition:** Selects elements where the attribute exactly matches the specified value.

**Syntax:**
```css
[attribute="value"] {
    property: value;
}
```

**Example:**
```css
[type="text"] {
    border: 1px solid #ccc;
}

[class="highlight"] {
    background-color: yellow;
}
```

### 3. Starts With [attribute^="value"]

**Definition:** Selects elements where the attribute value starts with the specified string.

**Syntax:**
```css
[attribute^="value"] {
    property: value;
}
```

**Example:**
```css
[href^="https"] {
    color: green;
}

[class^="btn"] {
    padding: 10px;
}
```

### 4. Ends With [attribute$="value"]

**Definition:** Selects elements where the attribute value ends with the specified string.

**Syntax:**
```css
[attribute$="value"] {
    property: value;
}
```

**Example:**
```css
[href$=".pdf"] {
    background: url(pdf-icon.png) no-repeat;
}

[src$=".jpg"] {
    border: 2px solid blue;
}
```

### 5. Contains [attribute*="value"]

**Definition:** Selects elements where the attribute value contains the specified substring.

**Syntax:**
```css
[attribute*="value"] {
    property: value;
}
```

**Example:**
```css
[href*="example"] {
    font-weight: bold;
}

[title*="important"] {
    color: red;
}
```

### 6. Contains Word [attribute~="value"]

**Definition:** Selects elements where the attribute contains the specified word as a complete word.

**Syntax:**
```css
[attribute~="value"] {
    property: value;
}
```

**Example:**
```css
[class~="active"] {
    background-color: blue;
}

[title~="help"] {
    cursor: help;
}
```

## Best Practices

1. Use attribute selectors for form styling
2. Target links based on their destination
3. Style elements based on data attributes
4. Combine with other selectors for specificity
5. Consider performance with complex attribute selectors