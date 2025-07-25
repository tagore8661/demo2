# Dynamic Pseudo Classes

## Dynamic Pseudo Classes Definition

Dynamic pseudo-classes are CSS selectors that target elements based on their current state or user interaction. These pseudo-classes respond to user actions like hovering, clicking, or focusing on elements, making web pages interactive and responsive.

**Key Feature:** Dynamic pseudo-classes change styling based on user behavior in real-time.

## Types of Dynamic Pseudo Classes

### 1. :hover

**Definition:** Applies styles when a user hovers over an element with a pointing device (like a mouse).

**Syntax:**
```css
selector:hover {
    property: value;
}
```

**Example:**
```css
button:hover {
    background-color: #0056b3;
    transform: scale(1.05);
}

a:hover {
    color: red;
    text-decoration: underline;
}
```

### 2. :active

**Definition:** Applies styles when an element is being activated (clicked or pressed).

**Syntax:**
```css
selector:active {
    property: value;
}
```

**Example:**
```css
button:active {
    background-color: #004085;
    transform: scale(0.95);
}

a:active {
    color: darkred;
}
```

### 3. :focus

**Definition:** Applies styles when an element has keyboard focus or is clicked.

**Syntax:**
```css
selector:focus {
    property: value;
}
```

**Example:**
```css
input:focus {
    border-color: #007bff;
    box-shadow: 0 0 5px rgba(0,123,255,0.5);
}

button:focus {
    outline: 2px solid #007bff;
}
```

### 4. :visited

**Definition:** Applies styles to links that have been visited by the user.

**Syntax:**
```css
a:visited {
    property: value;
}
```

**Example:**
```css
a:visited {
    color: purple;
}

.nav a:visited {
    color: #6c757d;
}
```

### 5. :link

**Definition:** Applies styles to unvisited links.

**Syntax:**
```css
a:link {
    property: value;
}
```

**Example:**
```css
a:link {
    color: blue;
    text-decoration: none;
}
```

## Interaction States Order

For links, CSS recommends the "LVHA" order:
1. **:link** - Unvisited links
2. **:visited** - Visited links  
3. **:hover** - Hovered links
4. **:active** - Active/clicked links

```css
a:link { color: blue; }
a:visited { color: purple; }
a:hover { color: red; }
a:active { color: darkred; }
```

## Common Use Cases

### Button Interactions
```css
.button {
    background-color: #007bff;
    transition: all 0.3s;
}

.button:hover {
    background-color: #0056b3;
    cursor: pointer;
}

.button:active {
    transform: translateY(1px);
}
```

### Form Elements
```css
input:focus {
    border-color: #007bff;
    outline: none;
}

input:hover {
    border-color: #6c757d;
}
```

## Best Practices

1. Always include :focus styles for accessibility
2. Use transitions for smooth hover effects
3. Follow the LVHA order for links
4. Provide visual feedback for all interactive elements
5. Test on both mouse and touch devices
6. Consider :focus-visible for better keyboard navigation