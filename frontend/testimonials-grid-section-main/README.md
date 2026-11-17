# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Links

- Live Site URL: [https://naoki-takami0120.github.io/learning/frontend/testimonials-grid-section-main](https://naoki-takami0120.github.io/learning/frontend/testimonials-grid-section-main)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- BEM naming

### What I learned

- **Grid vs Flexbox:** Some cards use two columns or two rows, so the page layout is two-dimensional. I used Grid for the page and Flexbox inside each card.
- **Sketching the grid first:** Before writing CSS, I drew the desktop layout as letters. Kira's card uses two rows, so it appears in both rows.

```
A A B C
D E E C
```

- **`grid-template-areas`:** I could write the sketch almost as it is. To make a card span two cells, I repeat its name. The names must be separated by spaces.

```css
grid-template-areas:
  "daniel  daniel  jonathan kira"
  "janette patrick patrick  kira";
grid-template-columns: repeat(4, 1fr);
```

- **`repeat()`:** The first argument is how many times, and the second is what to repeat. `repeat(1fr, 4)` is invalid, and the browser ignores it.
- **HTML order:** Screen readers and the Tab key follow the HTML order, not the visual position. I wrote the cards in the mobile order and moved Kira with Grid on desktop.
- **BEM blocks:** One testimonial card is a block (`testimonial`), not an element of the grid. I named modifiers by color (`testimonial--white`), so the two white cards share one rule.
- **Modifier + element:** To change only the heading in white cards, I combined the modifier and the element.

```css
.testimonial--white .testimonial__heading {
  color: var(--grey-500);
}
```

- **`:nth-child()` vs classes:** I used `:nth-child()` to place the cards, because the order will not change. If the order changes, it breaks without any error. A placement class is safer for real sites.
- **Contrast and `opacity`:** `opacity: 0.5` looked good on dark cards. But on the white card, the grey text became too light (about 2:1). I checked the contrast ratio in DevTools and removed the opacity on white cards.
- **Mobile first:** I set `max-width: 600px` for one column, and changed it to `1114px` in the media query for four columns.
- **Choosing a breakpoint:** 1440px is only the design size, not a breakpoint. I made the screen narrower in DevTools and chose `1024px`.
- **Centering vertically:** `justify-content: center` needs extra space in the parent. I gave `body` `min-height: 100vh` and made it a flex container.
- **Debugging:** A missing space in `@media screen and(min-width: ...)` made the whole media query invalid. DevTools helped me find which rules were applied.

### Continued development

In my last project, I wanted to try mobile-first and CSS Grid. I did both this time.

- Learn more about Grid, such as `grid-column` / `grid-row` and `auto-fit`.
- Check accessibility more, such as contrast ratio and 200% zoom, from the start of a project.

### AI Collaboration

- I used Claude Code as a mentor. It did not write my code.
- It reviewed my HTML and CSS, and gave me hints and questions instead of answers.
- It helped me find bugs, such as a wrong closing tag, an invalid media query, and wrong image paths.
- What worked well: I learned how to check things myself in DevTools.

## Author

- Frontend Mentor - [@naoki-takami0120](https://www.frontendmentor.io/profile/naoki-takami0120)
