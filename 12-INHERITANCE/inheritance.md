# CSS Inheritance

## Inheritance Definition

CSS Inheritance is a mechanism where certain CSS properties are automatically passed down from parent elements to their child elements. This means child elements can "inherit" styles from their parent elements without explicitly defining those styles.

**Think of it as:** Family traits that are passed from parents to children - just like how children might inherit eye color from their parents, HTML elements can inherit styling properties from their parent elements.

## How Does Inheritance Work in CSS?

### 1. Inherited Properties
Some CSS properties are inherited by default:

**Text-related properties:**
- `color`
- `font-family`
- `font-size`
- `font-weight`
- `line-height`
- `text-align`
- `text-transform`

**List properties:**
- `list-style`
- `list-style-type`

### 2. Non-Inherited Properties
Some properties are NOT inherited by default:

**Box model properties:**
- `margin`
- `padding`
- `border`
- `width`
- `height`

**Background properties:**
- `background-color`
- `background-image`

**Positioning properties:**
- `position`
- `top`, `right`, `bottom`, `left`

### 3. Inheritance Example

```css
/* Parent element */
.parent {
    color: blue;           /* Inherited */
    font-family: Arial;    /* Inherited */
    background-color: yellow; /* NOT inherited */
    padding: 20px;         /* NOT inherited */
}

/* Child elements automatically inherit color and font-family */
.parent p {
    /* color: blue; - automatically inherited */
    /* font-family: Arial; - automatically inherited */
    /* background-color: transparent; - NOT inherited */
    /* padding: 0; - NOT inherited */
}
```

## Controlling Inheritance

### 1. inherit Keyword
Forces a property to inherit from its parent:

```css
.child {
    background-color: inherit; /* Forces inheritance */
    margin: inherit;
}
```

### 2. initial Keyword
Sets a property to its default value:

```css
.child {
    color: initial; /* Resets to browser default */
}
```

### 3. unset Keyword
Uses inherited value if property inherits, otherwise uses initial value:

```css
.child {
    color: unset; /* Uses inherited value */
    margin: unset; /* Uses initial value (0) */
}
```

## Inheritance Chain

Inheritance works through multiple levels:

```html
<div class="grandparent">
    <div class="parent">
        <p class="child">Text inherits from all ancestors</p>
    </div>
</div>
```

```css
.grandparent { color: red; }
.parent { font-size: 18px; }
/* .child inherits both color: red and font-size: 18px */
```

## Benefits of Inheritance

1. **Reduces code repetition** - Don't need to set font-family on every element
2. **Maintains consistency** - Ensures uniform styling across related elements
3. **Easier maintenance** - Change parent style affects all children
4. **Smaller CSS files** - Less code needed for common properties

## Best Practices

1. **Set common styles on parent elements** (body, containers)
2. **Use inheritance for typography** (fonts, colors, text properties)
3. **Override inheritance when needed** using specific selectors
4. **Understand which properties inherit** to avoid unexpected results
5. **Use inherit keyword** to force inheritance when needed