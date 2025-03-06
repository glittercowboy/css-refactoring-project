# Base Styles

This document outlines the base styles implementation for the project, which provides foundational styling for HTML elements and accessibility features.

## Files Created

- `_base.scss` - Core styling for HTML elements
- `_accessibility.scss` - Styles that enhance accessibility 
- `_responsive.scss` - Media queries for responsive typography

## Base Styles Overview

The base styles provide consistent styling for fundamental HTML elements across the site:

### Typography

All typography is set using our variable system:

```scss
h1 {
  font-size: $font-size-h1;
  line-height: $line-height-tight;
}

h2 {
  font-size: $font-size-h2;
}
```

### Reset/Normalize

We've implemented a lightweight reset to ensure consistent rendering across browsers:

```scss
*, 
*::before, 
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

### Links

Links have consistent styling with hover states:

```scss
a {
  color: $color-primary;
  text-decoration: none;
  transition: $transition-base;
  
  &:hover,
  &:focus {
    color: darken($color-primary, 10%);
    text-decoration: underline;
  }
}
```

### Lists, Blockquotes, and Other Elements

We've provided consistent styling for other HTML elements like lists, blockquotes, code blocks, and form elements.

## Accessibility Features

The `_accessibility.scss` file includes:

### Focus Styles

```scss
:focus {
  outline: 2px solid $color-primary;
  outline-offset: 2px;
}
```

### Screen Reader Text

```scss
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}
```

### Reduced Motion

```scss
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

## Responsive Typography

The `_responsive.scss` file contains media queries that adjust typography sizes at different breakpoints:

```scss
@media (max-width: $breakpoint-md) {
  html {
    font-size: 16px;
  }

  body {
    font-size: 0.9rem;
  }

  h1 {
    font-size: 4.8rem;
  }
  // ...
}
```

## How To Use

To use these base styles, simply import them in your main SCSS file:

```scss
@import 'base';
@import 'accessibility';
@import 'responsive';
```

These styles provide a solid foundation for building more complex components and layouts.
