# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Links

- Live Site URL: [https://naoki-takami0120.github.io/learning/frontend/product-preview-card-component-main](https://naoki-takami0120.github.io/learning/frontend/product-preview-card-component-main)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Media queries

### What I learned

- **Mobile-first:** I wrote the mobile layout first. Then I used a media query to make the desktop layout.
- **Buttons vs links:** A link goes to another page. A button does an action. "Add to Cart" is an action, so I used `<button>`.
- **Responsive images:** I used `<picture>` to show a different image on mobile and desktop.
- **Old price:** I used `<s>` for the old price. It means "this is no longer correct."
- **`flex: 1` vs `flex-basis: 50%`:** `flex: 1` did not make two equal columns, because of the padding. `flex-basis: 50%` fixed it.

```css
.perfume-card__image,
.perfume-card__content {
  flex-basis: 50%;
}
```

- **`object-fit: cover`:** The image fills its box and keeps its shape.
- **Buttons and fonts:** A `<button>` does not use the page font by default. I added `font-family: inherit`.
- **`:focus-visible`:** It shows the focus style only for keyboard users. With `:focus`, the style also stayed after a mouse click.

### Continued development

- Understand how Flexbox decides the size of items.
- Learn more about CSS specificity and the order of rules.

## Author

- Frontend Mentor - [@naoki-takami0120](https://www.frontendmentor.io/profile/naoki-takami0120)
