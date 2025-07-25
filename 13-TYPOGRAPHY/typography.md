# CSS Typography

## Typography Definition

Typography in CSS refers to the styling and formatting of text content on web pages. It encompasses everything related to how text appears, including font selection, sizing, spacing, alignment, and decorative effects. Good typography enhances readability and creates visual hierarchy.

## Adding Fonts

### 1. System Fonts
Using fonts already installed on the user's system:

```css
body {
    font-family: Arial, sans-serif;
}

h1 {
    font-family: "Times New Roman", serif;
}
```

### 2. Web Fonts
Loading custom fonts from external sources:

```css
/* Using @import */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

/* Using link in HTML */
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
```

## Generic Font Families

CSS provides five generic font families as fallbacks:

### 1. serif
Fonts with decorative strokes (Times New Roman, Georgia):
```css
.serif-text {
    font-family: "Times New Roman", Georgia, serif;
}
```

### 2. sans-serif
Fonts without decorative strokes (Arial, Helvetica):
```css
.sans-serif-text {
    font-family: Arial, Helvetica, sans-serif;
}
```

### 3. monospace
Fixed-width fonts (Courier, Monaco):
```css
.monospace-text {
    font-family: "Courier New", Monaco, monospace;
}
```

### 4. cursive
Script-like fonts (Brush Script, Lucida Handwriting):
```css
.cursive-text {
    font-family: "Brush Script MT", cursive;
}
```

### 5. fantasy
Decorative fonts (Impact, Papyrus):
```css
.fantasy-text {
    font-family: Impact, fantasy;
}
```

## Google Fonts

Google Fonts provides free web fonts that can be easily integrated:

### 1. Using Link Tag (Recommended)
```html
<link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
```

### 2. Using @import
```css
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700&display=swap');
```

### 3. Using in CSS
```css
body {
    font-family: 'Open Sans', sans-serif;
}
```

## Font Styling

### 1. Font Weight
Controls the thickness of text:

```css
.light { font-weight: 300; }      /* Light */
.normal { font-weight: 400; }     /* Normal/Regular */
.medium { font-weight: 500; }     /* Medium */
.semibold { font-weight: 600; }   /* Semi-bold */
.bold { font-weight: 700; }       /* Bold */
.extrabold { font-weight: 800; }  /* Extra-bold */

/* Using keywords */
.bold-keyword { font-weight: bold; }
.normal-keyword { font-weight: normal; }
```

### 2. Font Style
Controls italic styling:

```css
.italic { font-style: italic; }
.oblique { font-style: oblique; }
.normal { font-style: normal; }
```

### 3. Font Size
Controls text size:

```css
.small { font-size: 12px; }
.medium { font-size: 16px; }
.large { font-size: 24px; }

/* Using relative units */
.em-size { font-size: 1.5em; }
.rem-size { font-size: 2rem; }
.percent-size { font-size: 120%; }
```

## Text Transform

Changes the capitalization of text:

```css
.uppercase { text-transform: uppercase; }    /* ALL CAPS */
.lowercase { text-transform: lowercase; }    /* all lowercase */
.capitalize { text-transform: capitalize; }  /* First Letter Of Each Word */
.none { text-transform: none; }             /* Original case */
```

## Text Decoration

Adds decorative lines to text:

```css
.underline { text-decoration: underline; }
.overline { text-decoration: overline; }
.line-through { text-decoration: line-through; }
.none { text-decoration: none; }

/* Multiple decorations */
.multiple { text-decoration: underline overline; }

/* Decoration styling */
.styled-underline {
    text-decoration: underline;
    text-decoration-color: red;
    text-decoration-style: wavy;
    text-decoration-thickness: 2px;
}
```

## Text Alignment

Controls horizontal alignment of text:

```css
.left { text-align: left; }
.center { text-align: center; }
.right { text-align: right; }
.justify { text-align: justify; }

/* Vertical alignment */
.top { vertical-align: top; }
.middle { vertical-align: middle; }
.bottom { vertical-align: bottom; }
```

## Additional Typography Properties

### Line Height
Controls spacing between lines:
```css
.tight { line-height: 1.2; }
.normal { line-height: 1.5; }
.loose { line-height: 2.0; }
```

### Letter Spacing
Controls spacing between characters:
```css
.tight-letters { letter-spacing: -1px; }
.normal-letters { letter-spacing: normal; }
.spaced-letters { letter-spacing: 2px; }
```

### Word Spacing
Controls spacing between words:
```css
.tight-words { word-spacing: -2px; }
.spaced-words { word-spacing: 5px; }
```

## Best Practices

1. **Limit font families** - Use 2-3 fonts maximum per project
2. **Ensure readability** - Maintain good contrast and appropriate sizes
3. **Use web-safe fallbacks** - Always include generic font families
4. **Optimize loading** - Use font-display: swap for better performance
5. **Consider accessibility** - Ensure text is readable for all users
6. **Test across devices** - Verify typography works on different screen sizes