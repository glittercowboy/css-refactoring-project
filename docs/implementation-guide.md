# Variables Implementation Guide

This guide shows how to implement the new variable system in your existing CSS to maintain the same visual design while improving code maintainability.

## Before & After Examples

### Example 1: Buttons

#### Before:
```css
.btn {
  border-color: #e6ac55;
  border-radius: 4px;
  background: #e6ac55;
  color: #0d0c0d;
}
.btn--outline {
  color: #e6ac55;
  background: transparent;
}
```

#### After:
```scss
.btn {
  border-color: $color-primary;
  border-radius: $border-radius;
  background: $color-primary;
  color: $color-dark;
  
  &--outline {
    color: $color-primary;
    background: transparent;
  }
}
```

### Example 2: Typography

#### Before:
```css
h1 {
  font-size: 6.61rem;
  line-height: 0.8;
}

h2 {
  font-size: 4.209rem;
}

h3 {
  font-size: 3.157rem;
}

h4 {
  font-size: 2.369rem;
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  font-style: normal;
}
```

#### After:
```scss
h1 {
  font-size: $font-size-h1;
  line-height: $line-height-tight;
}

h2 {
  font-size: $font-size-h2;
}

h3 {
  font-size: $font-size-h3;
}

h4 {
  font-size: $font-size-h4;
  font-family: $font-primary;
  font-weight: $font-weight-regular;
  font-style: normal;
}
```

### Example 3: Spacing & Layout

#### Before:
```css
.block {
  padding: 20px;
}

@media (min-width: 768px) {
  .block {
    padding: 30px;
  }
}

.container {
  max-width: calc(1260px + 10px + 10px);
  padding-right: 10px;
  padding-left: 10px;
}

@media (min-width: 768px) {
  .container {
    max-width: calc(1260px + 40px + 40px);
    padding-right: 40px;
    padding-left: 40px;
  }
}
```

#### After:
```scss
.block {
  padding: $spacing-block-mobile;
  
  @media (min-width: $breakpoint-md) {
    padding: $spacing-block-desktop;
  }
}

.container {
  max-width: calc(#{$container-width} + #{$container-padding-mobile} * 2);
  padding-right: $container-padding-mobile;
  padding-left: $container-padding-mobile;
  
  @media (min-width: $breakpoint-md) {
    max-width: calc(#{$container-width} + #{$container-padding-desktop} * 2);
    padding-right: $container-padding-desktop;
    padding-left: $container-padding-desktop;
  }
}
```

### Example 4: Backgrounds & Colors

#### Before:
```css
.section__overlay {
  background-color: rgba(236, 240, 241, 0.1);
}

.background-dark {
  background-color: #0d0c0d;
}

.background-light {
  background-color: #f0f0f0;
}

a.link-list__link {
  color: #0d0c0d;
}
```

#### After:
```scss
.section__overlay {
  background-color: rgba($color-light, 0.1);
}

.background-dark {
  background-color: $color-dark;
}

.background-light {
  background-color: $color-light;
}

a.link-list__link {
  color: $color-dark;
}
```

## Benefits of Using Variables

1. **Consistency**: All color, spacing, and typography values are consistent throughout the site
2. **Maintainability**: Need to change a color? Update it in one place instead of searching and replacing
3. **Scalability**: Makes it easier to add new components that adhere to the design system
4. **Readability**: Code becomes more semantic and easier to understand

## Implementation Strategy

1. Start with global elements (typography, containers, sections)
2. Move on to common components (buttons, navigation, cards)
3. Address specific page layouts and unique components
4. Test thoroughly to ensure visual consistency

## CSS Properties to Replace with Variables

| CSS Property | Variable to Use |
|--------------|----------------|
| `color` (for text) | `$color-dark`, `$color-light`, `$color-primary` |
| `background-color` | `$color-dark`, `$color-light`, `$color-primary`, `$color-white` |
| `border-color` | `$color-dark`, `$color-light`, `$color-primary` |
| `border-radius` | `$border-radius` |
| `font-family` | `$font-primary`, `$font-display` |
| `font-size` | `$font-size-h1` through `$font-size-h6`, `$font-size-base`, `$font-size-small` |
| `padding`, `margin` | `$spacing-xs`, `$spacing-sm`, `$spacing-md`, `$spacing-lg`, `$spacing-xl` |
| Media query breakpoints | `$breakpoint-sm`, `$breakpoint-md`, `$breakpoint-lg`, `$breakpoint-xl` |
