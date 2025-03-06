# UI Component Documentation

This document provides detailed information about the UI components created as part of the CSS refactoring project.

## Table of Contents

- [Button Component](#button-component)
- [Card Component](#card-component)
- [Form Component](#form-component)
- [Image Component](#image-component)
- [Feature Component](#feature-component)
- [Modal Component](#modal-component)
- [Alert Component](#alert-component)

## Button Component

The button component provides styled buttons with various modifiers for size, color, and style.

### Usage

```html
<button class="btn btn--solid btn--primary btn--medium">Primary Button</button>
<button class="btn btn--outline btn--dark">Outline Dark Button</button>
<a href="#" class="btn btn--solid btn--light btn--large">Light Link Button</a>
```

### Modifiers

- **Button Types**
  - `btn--solid`: Default filled button
  - `btn--outline`: Button with outline and transparent background

- **Button Colors**
  - `btn--primary`: Uses primary brand color
  - `btn--dark`: Uses dark color
  - `btn--light`: Uses light color

- **Button Sizes**
  - `btn--small`: Small button
  - `btn--medium`: Medium button (default)
  - `btn--large`: Large button

- **Button Widths**
  - `btn--auto`: Auto width (default)
  - `btn--full`: Full width of its container

### States

- `:hover`, `:focus`: Provides visual feedback
- `:disabled`, `.btn--disabled`: Indicates button is not interactive

## Card Component

The card component is a flexible container for grouping and displaying content.

### Usage

```html
<div class="card card--shadow">
  <div class="card__content">
    <h3 class="card__title">Card Title</h3>
    <p>Card content goes here.</p>
  </div>
</div>

<div class="card card--primary card--bordered">
  <img src="image.jpg" class="card__image" alt="Card image">
  <div class="card__content">
    <h3 class="card__title">Card with Image</h3>
    <p>Card content with image.</p>
  </div>
  <div class="card__footer">
    <button class="btn btn--solid btn--primary">Action</button>
  </div>
</div>
```

### Modifiers

- **Card Styles**
  - `card--shadow`: Card with drop shadow
  - `card--bordered`: Card with border
  - `card--dashed`: Card with dashed border (from original CSS)

- **Card Colors**
  - `card--primary`: Primary color background
  - `card--dark`: Dark background with light text
  - `card--light`: Light background

- **Card Layouts**
  - `card--horizontal`: Image on the side on larger screens
  - `card--link`: Card that acts as a link/clickable area
  - `card--feature`: Special styling for feature cards

## Form Component

The form component provides styling for form elements including inputs, textareas, selects, and checkboxes.

### Usage

```html
<div class="form">
  <div class="form__group">
    <label class="form__label" for="name">Name</label>
    <input type="text" id="name" class="form-control" placeholder="Enter your name">
    <span class="form__help-text">Enter your full name</span>
  </div>
  
  <div class="form__group">
    <label class="form__label" for="email">Email</label>
    <input type="email" id="email" class="form-control form-control--error" placeholder="Enter your email">
    <span class="form__error">Please enter a valid email address</span>
  </div>
  
  <button type="submit" class="form-btn">Submit</button>
</div>
```

### Components

- **Form Groups**
  - `.form__group`: Container for a label, input, and auxiliary text
  - `.form__label`: Label for form control
  - `.form__help-text`: Helper text below the control
  - `.form__error`: Error message for validation

- **Form Controls**
  - `.form-control`: Basic input styling
  - `.form-control--error`: For validation errors
  - `.form-control--success`: For successful validation
  - `.form-control--disabled`: For disabled inputs

- **Checkboxes and Radios**
  - `.form-check`: Container for checkboxes/radios
  - `.form-check__input`: The checkbox/radio input
  - `.form-check__label`: Label for the checkbox/radio

- **Form Layouts**
  - `.form-horizontal`: Horizontal form with labels beside inputs on larger screens

- **Form Button**
  - `.form-btn`: Submit button styled for forms

## Image Component

The image component provides flexible ways to display images with various styling options.

### Usage

```html
<div class="image image--rounded">
  <img src="image.jpg" class="image__image" alt="Description">
  <div class="image__overlay">
    <div class="image__overlay-text">Overlay text</div>
  </div>
</div>

<div class="image image--circle image--zoom">
  <img src="profile.jpg" class="image__image" alt="Profile">
</div>
```

### Modifiers

- **Border Radius**
  - `image--rounded`: Rounded corners
  - `image--circle`: Circular image
  - `image--no-radius`: No border radius

- **Size Options**
  - `image--auto-width`: Automatic width
  - `image--full-width`: 100% width
  - `image--fixed-width`: Fixed width (200px)

- **Aspect Ratio**
  - `image--square`: 1:1 aspect ratio
  - `image--16-9`: 16:9 aspect ratio

- **Effects**
  - `image--zoom`: Zoom effect on hover
  - `image--filter`: Grayscale filter that clears on hover

- **Container Alignment**
  - `image-container--center`: Center the image
  - `image-container--left`: Align left
  - `image-container--right`: Align right

## Feature Component

The feature component displays content with images and text, often used for showcasing services or testimonials.

### Usage

```html
<div class="feature feature--horizontal">
  <img src="feature.jpg" class="feature__image" alt="Feature">
  <div class="feature__text">
    <h3 class="feature__title">Feature Title</h3>
    <h4 class="feature__subtitle">Subtitle text</h4>
    <p class="feature__description">Description of the feature.</p>
  </div>
</div>

<div class="feature feature--box feature--primary">
  <img src="icon.png" class="feature__image feature__image--small" alt="Icon">
  <div class="feature__text">
    <h3 class="feature__title">Boxed Feature</h3>
    <p class="feature__description">This feature has a box around it.</p>
  </div>
</div>
```

### Modifiers

- **Layout Options**
  - `feature--horizontal`: Image and text side by side on larger screens
  - `feature--image-top`: Image above text (default)
  - `feature--image-bottom`: Image below text
  - `feature--image-right`: Image on the right (combined with horizontal)

- **Text Alignment**
  - `feature--text-left`: Left-aligned text
  - `feature--text-center`: Center-aligned text (default)
  - `feature--text-right`: Right-aligned text

- **Box Styles**
  - `feature--box`: Box container style
  - `feature--bordered`: Bordered container
  - `feature--dashed`: Dashed border (from original CSS)

- **Colors**
  - `feature--primary`: Primary color background
  - `feature--dark`: Dark background with light text
  - `feature--light`: Light background

- **Image Sizes**
  - `feature__image--small`: Small image (125px)
  - `feature__image--medium`: Medium image (200px)
  - `feature__image--large`: Large image (300px)

## Modal Component

The modal component creates dialog windows that appear on top of the main content.

### Usage

```html
<div class="modal" id="example-modal">
  <div class="modal__content">
    <div class="close-x">
      <div class="close-x__part"></div>
      <div class="close-x__part"></div>
    </div>
    <div class="modal__header">
      <h3 class="modal__title">Modal Title</h3>
    </div>
    <div class="modal__body">
      <p>Modal content goes here.</p>
    </div>
    <div class="modal__footer">
      <button class="btn btn--solid btn--primary">Confirm</button>
      <button class="btn btn--outline btn--primary">Cancel</button>
    </div>
  </div>
</div>
```

### Components

- **Modal Structure**
  - `.modal`: The modal container
  - `.modal__content`: The modal content container
  - `.modal__header`: Modal header section
  - `.modal__title`: Modal title
  - `.modal__body`: Main content area
  - `.modal__footer`: Modal footer, typically for actions

- **Modal Sizes**
  - `.modal--small`: Small modal
  - `.modal--medium`: Medium modal (default)
  - `.modal--large`: Large modal
  - `.modal--full`: Nearly full-screen modal

- **Modal Content Colors**
  - `.modal__content--dark`: Dark background with light text
  - `.modal__content--light`: Light background
  - `.modal__content--primary`: Primary color background

- **Close Button**
  - `.close-x`: Close button container
  - `.close-x__part`: Parts of the close X icon

## Alert Component

The alert component provides feedback messages and notifications.

### Usage

```html
<div class="alert alert--success">
  <div class="alert__content">
    <div class="alert__message">Operation completed successfully!</div>
  </div>
  <button class="alert__close">&times;</button>
</div>

<div class="alert alert--error alert--dismissible">
  <div class="alert__icon">⚠️</div>
  <div class="alert__content">
    <h4 class="alert__title">Error</h4>
    <div class="alert__message">An error occurred. Please try again.</div>
    <div class="alert__actions">
      <button class="btn btn--solid btn--small">Retry</button>
    </div>
  </div>
  <button class="alert__close">&times;</button>
</div>
```

### Modifiers

- **Alert Types**
  - `alert--primary`: Primary color alert
  - `alert--info`: Informational alert
  - `alert--success`: Success message
  - `alert--warning`: Warning message
  - `alert--error`: Error message (also `alert--danger`)

- **Alert Layout**
  - `alert--dismissible`: Alert with close button
  - `alert--border-left`: Alert with left border only
  - `alert--shadow`: Alert with drop shadow
  - `alert--outline`: Alert with outline only
  - `alert--rounded`: Alert with rounded corners

- **Alert Sizes**
  - `alert--small`: Small alert
  - `alert--large`: Large alert

- **Notification Types**
  - `alert--notification`: Fixed position notification
  - `alert--notification-top-right`: Top right corner
  - `alert--notification-top-left`: Top left corner
  - `alert--notification-bottom-right`: Bottom right corner
  - `alert--notification-bottom-left`: Bottom left corner
  - `alert--banner`: Full-width banner alert
