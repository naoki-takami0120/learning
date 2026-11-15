# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS).

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

- See hover and focus states for all interactive elements on the page

### Links

- Live Site URL: [https://naoki-takami0120.github.io/learning/frontend/blog-preview-card-main](https://naoki-takami0120.github.io/learning/frontend/blog-preview-card-main)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Media queries

### What I learned

- **Semantic HTML:** I used `<article>` for the card and `<time>` for the date.
- **Alt text:** Decorative images should have an empty `alt=""`.
- **BEM:** I named classes like `blog-card__title`.
- **Responsive images:** `max-width: 100%` stops images from overflowing.
- **Margin collapsing:** Vertical margins between blocks do not add up. The bigger one wins.
- **Media queries:** They go at the bottom of the CSS, because later rules win.

```css
:root {
  --yellow: rgb(244, 208, 78);
}
```

### Continued development

- Try a mobile-first workflow.
- Understand CSS specificity better.

## Author

- Frontend Mentor - [@naoki-takami0120](https://www.frontendmentor.io/profile/naoki-takami0120)
