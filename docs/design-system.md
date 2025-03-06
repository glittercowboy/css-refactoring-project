# Design System Documentation

This document outlines the design system used in the Heart of Sound website. It serves as a reference for designers and developers to maintain consistency across the site.

## Color Palette

The Heart of Sound website uses a focused color palette to create a strong brand identity:

### Primary Colors

- **Primary Gold** (`$color-primary: #e6ac55`): Used for buttons, highlights, and accent elements
- **Dark** (`$color-dark: #0d0c0d`): Used for text and backgrounds in dark sections
- **Light** (`$color-light: #f0f0f0`): Used for text on dark backgrounds and light section backgrounds
- **White** (`$color-white: #ffffff`): Used for backgrounds and text on dark backgrounds

### Secondary Colors

- **Link Color** (`$color-links: #595959`): Used for navigation links in their default state
- **Footer Background** (`$color-footer-bg: #161e2a`): Dark blue used for the footer background

### Status Colors

- **Error** (`$color-error: #d32f2f`): Used for error messages and validation
- **Success** (`$color-success: #388e3c`): Used for success messages and confirmations
- **Warning** (`$color-warning: #f57c00`): Used for warning messages and notifications
- **Info** (`$color-info: #1976d2`): Used for informational messages

## Typography

### Font Families

- **Primary Font**: Poppins (`$font-primary`)
  - Used for body text, headings, and UI elements
- **Display Font**: Abril Fatface (`$font-display`)
  - Used for special display text, primarily large headers

### Font Sizes

We use a modular scale with a base size of 18px (1rem):

- **Base**: 1rem (18px)
- **H1**: 6.61rem (118.98px)
- **H2**: 4.209rem (75.76px)
- **H3**: 3.157rem (56.83px)
- **H4**: 2.369rem (42.64px)
- **H5**: 1.777rem (31.99px)
- **H6**: 1.333rem (24px)
- **Small**: 0.889rem (16px)

### Font Weights

- **Thin**: 100
- **Light**: 300
- **Regular**: 400
- **Medium**: 500
- **Semibold**: 600
- **Bold**: 700
- **Black**: 900

## Spacing

We use a consistent spacing system based on the base unit of 1rem (18px):

- **XS**: 0.5rem (9px)
- **SM**: 1rem (18px)
- **MD**: 2rem (36px)
- **LG**: 3rem (54px)
- **XL**: 4rem (72px)
- **XXL**: 6rem (108px)

For component padding, we use:
- **Mobile**: 20px
- **Desktop**: 30px

## Breakpoints

The site uses the following breakpoints for responsive design:

- **Small**: 480px
- **Medium**: 768px
- **Large**: 1024px
- **Extra Large**: 1260px

## UI Elements

### Buttons

Buttons use the primary color with appropriate hover states and have a border radius of 4px.

### Cards & Containers

Content blocks have consistent padding (20px on mobile, 30px on desktop) and often use background colors from the palette.

### Borders & Shadows

- **Border Radius**: 4px for most UI elements
- **Border Width**: 2px for borders and outlines
- **Box Shadows**: Various levels of shadow for depth (none, small, medium, large)

## How to Use Variables

When writing SCSS, always use the variables defined in `_variables.scss` instead of hardcoded values:

```scss
// Instead of this:
.button {
  background-color: #e6ac55;
  padding: 18px 36px;
  border-radius: 4px;
}

// Do this:
.button {
  background-color: $color-primary;
  padding: $spacing-sm $spacing-md;
  border-radius: $border-radius;
}
```

This ensures consistency across the site and makes it easier to update the design in the future.
