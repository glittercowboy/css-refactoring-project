# Layout Components

This document outlines the layout components used in the project, which provide structural elements for building pages.

## Files Created

- `_layout.scss` - Core layout components like containers, grids, and sections
- `layout/_header.scss` - Header component styles
- `layout/_footer.scss` - Footer component styles
- `layout/_index.scss` - Import file for all layout components

## Layout Components Overview

The layout components provide the structural foundation of all pages:

### Container

The container component centers content and provides consistent horizontal padding:

```scss
.container {
  width: 100%;
  max-width: calc(#{$container-width} + #{$container-padding-mobile} * 2);
  padding-right: $container-padding-mobile;
  padding-left: $container-padding-mobile;
  margin-right: auto;
  margin-left: auto;
  
  @media (min-width: $breakpoint-md) {
    max-width: calc(#{$container-width} + #{$container-padding-desktop} * 2);
    padding-right: $container-padding-desktop;
    padding-left: $container-padding-desktop;
  }
}
```

### Section

Sections are used to group content with consistent vertical padding and background styles:

```scss
.section {
  position: relative;
  padding: $spacing-lg 0;
  
  &__overlay {
    position: absolute;
    width: 100%;
    height: 100%;
    left: 0;
    top: 0;
    z-index: 1;
  }
  
  .container {
    position: relative;
    z-index: 2;
  }
}
```

### Grid System

A flexbox-based grid system for creating responsive layouts:

```scss
.row {
  display: flex;
  flex-wrap: wrap;
  margin-right: -#{$spacing-sm / 2};
  margin-left: -#{$spacing-sm / 2};
}

.col {
  padding-right: $spacing-sm / 2;
  padding-left: $spacing-sm / 2;
  width: 100%;
  
  &--6 {
    width: 50%;
  }
  
  &--4 {
    width: 33.333333%;
  }
  
  // etc...
}
```

### Block

Blocks are content containers used within sections:

```scss
.block {
  position: relative;
  width: 100%;
  
  &--padded {
    padding: $spacing-block-mobile;
    
    @media (min-width: $breakpoint-md) {
      padding: $spacing-block-desktop;
    }
  }
}
```

## Header Component

The header component includes:

- Logo
- Navigation links
- User menu
- Responsive behaviors
- Dropdown menus

Key features:

```scss
.header {
  background-color: $color-white;
  font-size: 18px;
  
  // Sticky header behavior
  &--sticky {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
  }
  
  // Overlay header style
  &--overlay {
    position: absolute;
    background-color: transparent;
  }
}
```

## Footer Component

The footer component includes:

- Logo
- Link lists
- Social icons
- Copyright notice
- Newsletter form

Key features:

```scss
.footer {
  background-color: $color-footer-bg;
  color: $color-light;
  padding: $spacing-lg 0;
  
  // Make footer take up remaining screen space if content is short
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}
```

## How To Use

### Container and Section

Use container and section components to structure page content:

```html
<section class="section background-light">
  <div class="section__overlay"></div>
  <div class="container">
    <!-- Content goes here -->
  </div>
</section>
```

### Grid System

Use the grid system to create responsive layouts:

```html
<div class="row">
  <div class="col col--12 col--md-6">
    <!-- Left column content -->
  </div>
  <div class="col col--12 col--md-6">
    <!-- Right column content -->
  </div>
</div>
```

### Header and Footer

The header and footer components are typically used at the top and bottom of each page, respectively:

```html
<header class="header">
  <!-- Header content -->
</header>

<main>
  <!-- Page content -->
</main>

<footer class="footer">
  <!-- Footer content -->
</footer>
```
