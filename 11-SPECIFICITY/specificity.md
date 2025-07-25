# CSS Specificity

## Specificity Definition

CSS Specificity is a set of rules that determines which CSS styles are applied to an element when multiple conflicting styles target the same element. It's like a scoring system that helps the browser decide which style rule should win when there are conflicts.

**Think of it as:** A point system where different selectors have different point values, and the selector with the highest total points wins.

## Specificity Hierarchy

CSS specificity follows a hierarchy from highest to lowest priority:

### 1. Inline Styles (1000 points)
```html
<p style="color: red;">Highest priority</p>
```

### 2. IDs (100 points)
```css
#header { color: blue; }
```

### 3. Classes, Attributes, Pseudo-classes (10 points)
```css
.highlight { color: green; }
[type="text"] { color: yellow; }
:hover { color: purple; }
```

### 4. Elements and Pseudo-elements (1 point)
```css
p { color: black; }
::before { color: gray; }
```

### 5. Universal Selector (0 points)
```css
* { color: inherit; }
```

## How to Calculate Specificity

Specificity is calculated using a four-part value: **a-b-c-d**

- **a** = Inline styles (1 or 0)
- **b** = Number of IDs
- **c** = Number of classes, attributes, and pseudo-classes
- **d** = Number of elements and pseudo-elements

### Examples:

```css
/* Specificity: 0-0-0-1 (1 point) */
p { color: red; }

/* Specificity: 0-0-1-0 (10 points) */
.highlight { color: blue; }

/* Specificity: 0-1-0-0 (100 points) */
#header { color: green; }

/* Specificity: 0-1-1-1 (111 points) */
#header .nav p { color: purple; }

/* Specificity: 1-0-0-0 (1000 points) */
<p style="color: orange;">Inline style</p>
```

## Specificity Rules

### 1. Higher Specificity Wins
```css
p { color: red; }           /* Specificity: 1 */
.text { color: blue; }      /* Specificity: 10 - This wins */
```

### 2. Equal Specificity - Last Rule Wins
```css
.highlight { color: red; }   /* Same specificity */
.highlight { color: blue; }  /* This wins (comes last) */
```

### 3. !important Override
```css
p { color: red !important; }  /* Overrides higher specificity */
#header { color: blue; }      /* Higher specificity but loses */
```

## Best Practices

1. **Keep specificity low** for easier maintenance
2. **Avoid !important** unless absolutely necessary
3. **Use classes** instead of IDs for styling
4. **Organize CSS** from general to specific
5. **Use meaningful class names** instead of complex selectors

## Common Specificity Problems

### Problem: Overly Specific Selectors
```css
/* Too specific - hard to override */
div.container ul.menu li.item a.link { color: blue; }

/* Better approach */
.menu-link { color: blue; }
```

### Problem: !important Overuse
```css
/* Avoid this */
.text { color: red !important; }

/* Better approach */
.special-text { color: red; }
```