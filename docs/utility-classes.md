# Utility Classes Documentation

This document provides a reference for all available utility classes in the Heart of Sound website. These utility classes allow for quick styling adjustments without writing custom CSS.

## Table of Contents

1. [Spacing Utilities](#spacing-utilities)
2. [Typography Utilities](#typography-utilities)
3. [Display Utilities](#display-utilities)
4. [Color Utilities](#color-utilities)
5. [Border Utilities](#border-utilities)
6. [Effect Utilities](#effect-utilities)
7. [Responsive Utilities](#responsive-utilities)

## Spacing Utilities

Spacing utilities help control the margin and padding of elements.

### Margin

```html
<!-- Margin on all sides -->
<div class="m-0">No margin</div>
<div class="m-1">Extra small margin (0.5rem)</div>
<div class="m-2">Small margin (1rem)</div>
<div class="m-3">Medium margin (2rem)</div>
<div class="m-4">Large margin (3rem)</div>
<div class="m-5">Extra large margin (4rem)</div>
<div class="m-auto">Auto margin</div>

<!-- Directional margin -->
<div class="mt-3">Margin top</div>
<div class="mr-3">Margin right</div>
<div class="mb-3">Margin bottom</div>
<div class="ml-3">Margin left</div>

<!-- Horizontal and vertical margin -->
<div class="mx-3">Horizontal margin</div>
<div class="my-3">Vertical margin</div>
```

### Padding

```html
<!-- Padding on all sides -->
<div class="p-0">No padding</div>
<div class="p-1">Extra small padding (0.5rem)</div>
<div class="p-2">Small padding (1rem)</div>
<div class="p-3">Medium padding (2rem)</div>
<div class="p-4">Large padding (3rem)</div>
<div class="p-5">Extra large padding (4rem)</div>

<!-- Directional padding -->
<div class="pt-3">Padding top</div>
<div class="pr-3">Padding right</div>
<div class="pb-3">Padding bottom</div>
<div class="pl-3">Padding left</div>

<!-- Horizontal and vertical padding -->
<div class="px-3">Horizontal padding</div>
<div class="py-3">Vertical padding</div>
```

## Typography Utilities

Typography utilities help style text.

### Text Alignment

```html
<p class="text-left">Left aligned text</p>
<p class="text-center">Center aligned text</p>
<p class="text-right">Right aligned text</p>
<p class="text-justify">Justified text</p>
```

### Font Families

```html
<p class="font-primary">Primary font (Poppins)</p>
<p class="font-display">Display font (Abril Fatface)</p>
```

### Font Weights

```html
<p class="font-thin">Thin text (100)</p>
<p class="font-light">Light text (300)</p>
<p class="font-regular">Regular text (400)</p>
<p class="font-medium">Medium text (500)</p>
<p class="font-semibold">Semibold text (600)</p>
<p class="font-bold">Bold text (700)</p>
<p class="font-black">Black text (900)</p>
```

### Font Sizes

```html
<p class="text-xs">Extra small text</p>
<p class="text-base">Base text size</p>
<p class="text-h6">H6 size</p>
<p class="text-h5">H5 size</p>
<p class="text-h4">H4 size</p>
<p class="text-h3">H3 size</p>
<p class="text-h2">H2 size</p>
<p class="text-h1">H1 size</p>
```

### Line Heights

```html
<p class="leading-tight">Tight line height (0.8)</p>
<p class="leading-heading">Heading line height (1.1)</p>
<p class="leading-normal">Normal line height (1.5)</p>
<p class="leading-loose">Loose line height (1.8)</p>
```

### Text Transforms

```html
<p class="text-uppercase">UPPERCASE TEXT</p>
<p class="text-lowercase">lowercase text</p>
<p class="text-capitalize">Capitalized Text</p>
<p class="text-normal-case">Normal case text</p>
```

## Display Utilities

Display utilities control the display and layout of elements.

### Display Types

```html
<div class="d-none">Not displayed</div>
<div class="d-inline">Inline element</div>
<div class="d-inline-block">Inline-block element</div>
<div class="d-block">Block element</div>
<div class="d-flex">Flex container</div>
<div class="d-grid">Grid container</div>
```

### Flex Container

```html
<!-- Flex direction -->
<div class="d-flex flex-row">Row (default)</div>
<div class="d-flex flex-column">Column</div>
<div class="d-flex flex-row-reverse">Row reverse</div>
<div class="d-flex flex-column-reverse">Column reverse</div>

<!-- Flex wrap -->
<div class="d-flex flex-wrap">Wrapped items</div>
<div class="d-flex flex-nowrap">No wrap</div>

<!-- Justify content -->
<div class="d-flex justify-content-start">Start</div>
<div class="d-flex justify-content-end">End</div>
<div class="d-flex justify-content-center">Center</div>
<div class="d-flex justify-content-between">Space between</div>
<div class="d-flex justify-content-around">Space around</div>

<!-- Align items -->
<div class="d-flex align-items-start">Start</div>
<div class="d-flex align-items-end">End</div>
<div class="d-flex align-items-center">Center</div>
<div class="d-flex align-items-baseline">Baseline</div>
<div class="d-flex align-items-stretch">Stretch</div>
```

### Flex Items

```html
<div class="flex-grow-0">No grow</div>
<div class="flex-grow-1">Grow</div>
<div class="flex-shrink-0">No shrink</div>
<div class="flex-shrink-1">Shrink</div>
<div class="flex-fill">Fill available space</div>
<div class="align-self-start">Self align start</div>
<div class="align-self-center">Self align center</div>
<div class="align-self-end">Self align end</div>
```

### Order

```html
<div class="order-first">First item</div>
<div class="order-0">Order 0</div>
<div class="order-1">Order 1</div>
<div class="order-2">Order 2</div>
<div class="order-last">Last item</div>
```

## Color Utilities

Color utilities allow for easy color application to text and backgrounds.

### Text Colors

```html
<p class="text-primary">Primary color text</p>
<p class="text-dark">Dark color text</p>
<p class="text-light">Light color text</p>
<p class="text-white">White text</p>
<p class="text-link">Link color text</p>
<p class="text-success">Success color text</p>
<p class="text-error">Error color text</p>
<p class="text-warning">Warning color text</p>
<p class="text-info">Info color text</p>
```

### Background Colors

```html
<div class="bg-primary">Primary background</div>
<div class="bg-dark">Dark background</div>
<div class="bg-light">Light background</div>
<div class="bg-white">White background</div>
<div class="bg-success">Success background</div>
<div class="bg-error">Error background</div>
<div class="bg-warning">Warning background</div>
<div class="bg-info">Info background</div>
<div class="bg-transparent">Transparent background</div>
```

### Background Images

```html
<div class="bg-cover">Background image with cover</div>
<div class="bg-contain">Background image with contain</div>
<div class="bg-center">Background image centered</div>
<div class="bg-no-repeat">Background image not repeated</div>
```

## Border Utilities

Border utilities control the borders of elements.

### Border Width

```html
<div class="border">Default border</div>
<div class="border-0">No border</div>
<div class="border-top">Top border only</div>
<div class="border-right">Right border only</div>
<div class="border-bottom">Bottom border only</div>
<div class="border-left">Left border only</div>
```

### Border Style

```html
<div class="border border-solid">Solid border</div>
<div class="border border-dashed">Dashed border</div>
<div class="border border-dotted">Dotted border</div>
<div class="border border-double">Double border</div>
```

### Border Radius

```html
<div class="rounded">Default rounded corners</div>
<div class="rounded-sm">Small rounded corners</div>
<div class="rounded-lg">Large rounded corners</div>
<div class="rounded-full">Fully rounded (circle/pill)</div>
<div class="rounded-0">No rounded corners</div>
<div class="rounded-top">Top corners rounded</div>
<div class="rounded-right">Right corners rounded</div>
<div class="rounded-bottom">Bottom corners rounded</div>
<div class="rounded-left">Left corners rounded</div>
```

## Effect Utilities

Effect utilities add visual effects to elements.

### Shadows

```html
<div class="shadow-none">No shadow</div>
<div class="shadow-sm">Small shadow</div>
<div class="shadow">Regular shadow</div>
<div class="shadow-lg">Large shadow</div>
```

### Opacity

```html
<div class="opacity-0">Invisible (0% opacity)</div>
<div class="opacity-25">25% opacity</div>
<div class="opacity-50">50% opacity</div>
<div class="opacity-75">75% opacity</div>
<div class="opacity-100">Fully visible (100% opacity)</div>
```

### Transforms

```html
<div class="scale-75">Scaled down to 75%</div>
<div class="scale-100">Normal scale (100%)</div>
<div class="scale-125">Scaled up to 125%</div>
<div class="rotate-90">Rotated 90 degrees</div>
<div class="rotate-180">Rotated 180 degrees</div>
```

### Transitions

```html
<div class="transition">Default transition</div>
<div class="transition-fast">Fast transition</div>
<div class="transition-slow">Slow transition</div>
<div class="transition-none">No transition</div>
```

### Hover Effects

```html
<div class="hover-grow">Grows on hover</div>
<div class="hover-shadow">Shows shadow on hover</div>
```

## Responsive Utilities

Responsive utilities change behavior across different screen sizes.

### Responsive Display

```html
<div class="d-block d-md-none">Visible on mobile only</div>
<div class="d-none d-md-block">Visible on desktop only</div>
<div class="hidden--mobile">Hidden on mobile</div>
<div class="hidden--desktop">Hidden on desktop</div>
```

### Responsive Text Alignment

```html
<p class="text-center text-md-left">Centered on mobile, left-aligned on desktop</p>
<p class="text-left text-md-center">Left-aligned on mobile, centered on desktop</p>
```

### Responsive Order

```html
<div class="order-2 order-md-1">Second on mobile, first on desktop</div>
<div class="order-1 order-md-2">First on mobile, second on desktop</div>
```

## Combining Utilities

Utility classes can be combined to create complex layouts without writing custom CSS:

```html
<div class="d-flex flex-column flex-md-row justify-content-between align-items-center p-3 mb-4 bg-light rounded shadow">
  <div class="text-center text-md-left mb-2 mb-md-0">
    <h2 class="text-primary font-bold mb-1">Example Card</h2>
    <p class="text-dark m-0">This card uses multiple utility classes for styling.</p>
  </div>
  <div>
    <button class="bg-primary text-dark p-2 rounded border-0 hover-grow transition">
      Click Me
    </button>
  </div>
</div>
```

## Strategy for Using Utilities

- Use utility classes for one-off styling needs
- For repeated patterns, create components instead
- Prioritize utility classes in this order:
  1. Layout (display, flex, etc.)
  2. Spacing (margin, padding)
  3. Sizing (width, height)
  4. Typography
  5. Visual styles (colors, borders, effects)
- Combine with responsive utilities to create adaptive interfaces
- Keep specificity in mind: utilities use `!important` to override component styles

## Benefits of Utility Classes

- **Rapid development**: Apply styles directly in HTML without writing CSS
- **Consistency**: All utilities use values from the design system
- **Reduced CSS size**: No need to create custom classes for one-off styling needs
- **Clear intent**: The purpose of each element's styling is visible in the HTML
- **Responsive design**: Easily adapt layouts for different screen sizes

## When to Create Components Instead

While utility classes are powerful, there are times when components are more appropriate:

- For complex UI elements that are reused throughout the site
- When the HTML structure becomes too cluttered with utilities
- For patterns that require specific JavaScript behavior
- When the design requires complex layouts that would be verbose with utilities

In these cases, extract the pattern into a component and use utility classes for fine-tuning.