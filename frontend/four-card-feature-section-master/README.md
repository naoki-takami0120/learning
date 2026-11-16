# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK).

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

- View the optimal layout for the site depending on their device's screen size

### Links

- Live Site URL: [https://naoki-takami0120.github.io/learning/frontend/four-card-feature-section-master](https://naoki-takami0120.github.io/learning/frontend/four-card-feature-section-master)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Media queries

### What I learned

- **Planning the layout:** I split the desktop design into three columns. The middle column has two cards stacked on top of each other.
- **BEM blocks:** A reusable part should be its own block. I used `card` for all four cards, and modifiers like `card--karma` for the different top colors.
- **Modifier names:** I named modifiers by content (`card--supervisor`), not by color (`card--cyan`). If the color changes, the HTML stays the same.
- **Inline vs block:** A `<span>` is inline, so it does not start a new line. I added `display: block` to put "Powered by Technology" on the second line.
- **`align-items` vs `align-self`:** `align-items` is set on the parent and moves all children. `align-self` is set on one child and moves only that child. I used it to move the icon to the right.

```css
.card__icon {
  align-self: flex-end;
}
```

- **The cross axis:** `align-items` works at a right angle to `flex-direction`. In a row, it controls the vertical position. In a column, it controls the horizontal position.
- **`center` vs `stretch`:** In the mobile layout, `align-items: center` made the cards different widths. `stretch` made them the same width, but they moved to the left because of `max-width`. I fixed it by giving the container the same `max-width` and `margin: auto`.
- **Choosing a breakpoint:** Three cards need about 1130px (350px × 3 + gaps). So I switch to one column below 1200px.
- **Soft shadows:** A big blur and a transparent color make the shadow look soft.

```css
box-shadow: 0px 5px 10px rgb(0, 0, 0, 0.2);
```

### Continued development

- Try a mobile-first workflow again. This time I wrote the desktop layout first.
- Learn CSS Grid and compare it with Flexbox for this kind of layout.

## Author

- Frontend Mentor - [@naoki-takami0120](https://www.frontendmentor.io/profile/naoki-takami0120)
