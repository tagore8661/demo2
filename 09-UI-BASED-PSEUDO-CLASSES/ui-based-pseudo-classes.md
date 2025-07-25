# UI-Based Pseudo Classes

## UI-Based Pseudo Classes Definition

UI-based pseudo-classes target form elements and user interface components based on their current state or properties. These selectors are particularly useful for styling form controls, providing visual feedback, and enhancing user experience in interactive applications.

**Purpose:** Style form elements based on their functional state rather than user interaction.

## Types of UI-Based Pseudo Classes

### 1. :enabled

**Definition:** Selects form elements that are enabled and can be interacted with.

**Syntax:**
```css
selector:enabled {
    property: value;
}
```

**Example:**
```css
input:enabled {
    background-color: white;
    border-color: #ced4da;
}

button:enabled {
    cursor: pointer;
    opacity: 1;
}
```

### 2. :disabled

**Definition:** Selects form elements that are disabled and cannot be interacted with.

**Syntax:**
```css
selector:disabled {
    property: value;
}
```

**Example:**
```css
input:disabled {
    background-color: #f8f9fa;
    color: #6c757d;
    cursor: not-allowed;
}

button:disabled {
    opacity: 0.5;
    cursor: not-allowed;
}
```

### 3. :checked

**Definition:** Selects checkboxes, radio buttons, or option elements that are checked/selected.

**Syntax:**
```css
selector:checked {
    property: value;
}
```

**Example:**
```css
input[type="checkbox"]:checked {
    background-color: #007bff;
    border-color: #007bff;
}

input[type="radio"]:checked {
    background-color: #28a745;
}
```

### 4. :required

**Definition:** Selects form elements that have the required attribute.

**Syntax:**
```css
selector:required {
    property: value;
}
```

**Example:**
```css
input:required {
    border-left: 3px solid #dc3545;
}

textarea:required {
    background-color: #fff5f5;
}
```

### 5. :optional

**Definition:** Selects form elements that do not have the required attribute.

**Syntax:**
```css
selector:optional {
    property: value;
}
```

**Example:**
```css
input:optional {
    border-left: 3px solid #28a745;
}
```

### 6. :valid

**Definition:** Selects form elements with valid input according to their type and constraints.

**Syntax:**
```css
selector:valid {
    property: value;
}
```

**Example:**
```css
input:valid {
    border-color: #28a745;
    background-color: #f8fff9;
}
```

### 7. :invalid

**Definition:** Selects form elements with invalid input according to their type and constraints.

**Syntax:**
```css
selector:invalid {
    property: value;
}
```

**Example:**
```css
input:invalid {
    border-color: #dc3545;
    background-color: #fff5f5;
}
```

### 8. :read-only

**Definition:** Selects elements that are read-only and cannot be edited.

**Syntax:**
```css
selector:read-only {
    property: value;
}
```

**Example:**
```css
input:read-only {
    background-color: #e9ecef;
    color: #495057;
}
```

### 9. :read-write

**Definition:** Selects elements that are editable by the user.

**Syntax:**
```css
selector:read-write {
    property: value;
}
```

**Example:**
```css
input:read-write {
    background-color: white;
    border: 2px solid #ced4da;
}
```

## Common Combinations

### Form Validation Styling
```css
/* Required fields */
input:required:invalid {
    border-color: #dc3545;
}

input:required:valid {
    border-color: #28a745;
}

/* Optional fields */
input:optional {
    border-style: dashed;
}
```

### Interactive States
```css
/* Enabled vs Disabled */
button:enabled:hover {
    background-color: #0056b3;
}

button:disabled {
    opacity: 0.6;
    cursor: not-allowed;
}
```

## Best Practices

1. Provide clear visual feedback for form states
2. Use :invalid and :valid for real-time validation feedback
3. Style :disabled elements to clearly show they're not interactive
4. Combine with other pseudo-classes for comprehensive form styling
5. Consider accessibility when styling form states
6. Test form styling across different browsers