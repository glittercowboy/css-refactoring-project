# Responsive Design Approach

This document outlines the responsive design approach used in the Heart of Sound website CSS refactoring project. It covers our mobile-first methodology, breakpoint system, and how to use the responsive mixins effectively.

## Mobile-First Philosophy

We follow a mobile-first approach to responsive design, which means:

1. **Start with mobile designs**: We build the base styles for mobile devices first
2. **Progressive enhancement**: We then add complexity and features as screen sizes increase
3. **Use min-width queries**: Our media queries use `min-width` to target larger screens
4. **Optimize for performance**: Mobile-first typically leads to more efficient CSS with less overrides

This approach ensures that our site works well on all devices, with special attention to the mobile experience, which represents a significant portion of web traffic.

## Breakpoint System

Our breakpoint system uses standardized screen sizes based on common device dimensions:

| Name | Value | Description |
|------|-------|-------------|
| `$breakpoint-sm` | 480px | Small mobile devices and up |
| `$breakpoint-md` | 768px | Tablets and medium-sized devices and up |
| `$breakpoint-lg` | 1024px | Laptops and desktops and up |
| `$breakpoint-xl` | 1260px | Large desktops and up |

## Using the Responsive Mixins

We've created a set of mixins in `_breakpoints.scss` to make writing responsive styles easier and more consistent.

### Mobile-First Mixins (min-width)

```scss
// For small devices and up (480px+)
@include sm-up {
  // Your styles here
}

// For medium devices and up (768px+)
@include md-up {
  // Your styles here
}

// For large devices and up (1024px+)
@include lg-up {
  // Your styles here
}

// For extra large devices and up (1260px+)
@include xl-up {
  // Your styles here
}
```

### Device-Specific Mixins (max-width or ranges)

```scss
// Only for extra small devices (up to 479px)
@include xs-only {
  // Your styles here
}

// Only for small devices (480px to 767px)
@include sm-only {
  // Your styles here
}

// Only for medium devices (768px to 1023px)
@include md-only {
  // Your styles here
}

// Only for large devices (1024px to 1259px)
@include lg-only {
  // Your styles here
}
```

### Custom Range Mixins

```scss
// For a custom range of screen sizes
@include between(600px, 900px) {
  // Your styles here
}
```

### Orientation and Feature Mixins

```scss
// For devices in portrait orientation
@include portrait {
  // Your styles here
}

// For devices in landscape orientation
@include landscape {
  // Your styles here
}

// For high-resolution (Retina) displays
@include retina {
  // Your styles here
}

// For devices with hover capability (typically non-touch devices)
@include has-hover {
  // Your styles here
}

// For devices without hover capability (typically touch devices)
@include no-hover {
  // Your styles here
}
```

## Best Practices

When writing responsive CSS using our system, follow these best practices:

### 1. Start with Base Styles

Write your base styles without media queries first, targeting mobile devices:

```scss
.card {
  padding: $spacing-sm;
  margin-bottom: $spacing-md;
  width: 100%;
}
```

### 2. Add Responsive Enhancements

Then progressively enhance for larger screens:

```scss
.card {
  padding: $spacing-sm;
  margin-bottom: $spacing-md;
  width: 100%;
  
  @include md-up {
    padding: $spacing-md;
    margin-bottom: $spacing-lg;
  }
  
  @include lg-up {
    width: 33.333%;
    float: left;
  }
}
```

### 3. Use Responsive Utility Classes When Appropriate

For simple adjustments, use our utility classes instead of writing custom media queries:

```html
<div class="text-center text-md-left">
  This text is centered on mobile but left-aligned on medium screens and up.
</div>

<div class="d-none d-md-block">
  This element is hidden on mobile but visible on medium screens and up.
</div>
```

### 4. Group Media Queries Together When Possible

For better readability, group related media queries together:

```scss
// Good
.element {
  // Base styles
  
  @include md-up {
    // Medium screen styles
  }
  
  @include lg-up {
    // Large screen styles
  }
}

// Avoid
.element {
  // Base styles
}

@include md-up {
  .element {
    // Medium screen styles
  }
}

@include lg-up {
  .element {
    // Large screen styles
  }
}
```

### 5. Consider Performance

Be mindful of performance implications:

- Avoid unnecessary media queries for minor adjustments
- Use the cascade and inheritance when possible
- Consider using the `@content` feature of Sass mixins judiciously

## Testing Responsive Designs

Always test responsive designs on actual devices or using device emulation in browser developer tools. Key testing points:

1. Test at each defined breakpoint
2. Test between breakpoints to catch edge cases
3. Test orientation changes on mobile devices
4. Test with different font sizes and zoom levels
5. Test with touch interactions on touch devices

## Implementation in Our Project

Our responsive implementation is organized into these files:

1. `scss/responsive/_breakpoints.scss` - Media query mixins
2. `scss/responsive/_typography.scss` - Responsive typography adjustments
3. `scss/responsive/_layout.scss` - Responsive layout adjustments
4. `scss/responsive/_navigation.scss` - Responsive navigation components
5. `scss/responsive/_utilities.scss` - Responsive utility classes
6. `scss/responsive/_index.scss` - Imports all responsive partials

All of these files are then imported via the main `scss/main.scss` file.
