# SCSS Directory

This directory contains the organized SCSS files that make up our refactored CSS architecture.

## File Structure

- `_variables.scss` - Design tokens (colors, typography, spacing, breakpoints)
- `_base.scss` - Base element styling and normalization
- `_layout.scss` - Layout components (containers, grid system)
- `_components.scss` - UI components (buttons, cards, forms)
- `_utilities.scss` - Utility classes for common styling needs
- `_responsive.scss` - Responsive behavior and media queries
- `main.scss` - Main entry file that imports all partials

## Naming Conventions

- All partial files are prefixed with an underscore `_`
- Class names use BEM (Block Element Modifier) methodology
- Variables use the following format: `$category-property-variant`

## How to Use

1. Make changes to the appropriate partial file
2. Compile the main.scss file to generate the final CSS
