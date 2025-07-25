# Sibling Selectors

## Sibling Selectors Definition

Sibling selectors target elements that share the same parent element. These selectors allow you to style elements based on their relationship with neighboring elements (siblings) in the HTML structure.

**Key Concept:** Siblings are elements at the same level in the HTML hierarchy that have the same parent element.

## Types of Sibling Selectors

### 1. Adjacent Sibling Selector (+)

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
    margin-top: 0;
}

.button + .button {
    margin-left: 10px;
}
```

**Use Case:** Style elements that come directly after specific elements.

### 2. General Sibling Selector (~)

**Definition:** Selects all elements that are siblings and come after a specified element.

**Syntax:**
```css
element1 ~ element2 {
    property: value;
}
```

**Example:**
```css
h2 ~ p {
    color: gray;
    line-height: 1.6;
}

.active ~ .item {
    opacity: 0.5;
}
```

**Use Case:** Style all following siblings, not just the immediate one.

## Key Differences

| Selector | Symbol | Targets | Example |
|----------|--------|---------|---------|
| Adjacent Sibling | + | Immediate next sibling | `h1 + p` |
| General Sibling | ~ | All following siblings | `h1 ~ p` |

## Practical Examples

### Adjacent Sibling (+)
```css
/* Style paragraph immediately after heading */
h2 + p {
    font-size: 18px;
    color: #333;
}

/* Add margin between consecutive buttons */
button + button {
    margin-left: 15px;
}
```

### General Sibling (~)
```css
/* Style all paragraphs after a heading */
h3 ~ p {
    text-indent: 20px;
}

/* Fade out items after active item */
.active ~ .menu-item {
    opacity: 0.6;
}
```

## Best Practices

1. Use adjacent sibling (+) for immediate styling relationships
2. Use general sibling (~) when you need to affect multiple following elements
3. Combine with other selectors for more specific targeting
4. Consider the HTML structure when planning sibling relationships
5. Test thoroughly as sibling relationships can be fragile with HTML changes