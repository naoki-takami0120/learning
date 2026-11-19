# Frontend Mentor - Meet landing page solution

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR).

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

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Links

- Live Site URL: [https://naoki-takami0120.github.io/learning/frontend/meet-landing-page/starter-code](https://naoki-takami0120.github.io/learning/frontend/meet-landing-page/starter-code)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- BEM naming

### What I learned

- **`<picture>` shows only one image:** On desktop, the hero has two images (left and right). So I put all the images in the HTML and switched them with `display: none` in media queries.
- **Flexbox works only on direct children:** To put only some items in a row, I wrapped them in a `div` (`.hero__buttons`, `.experience__content`).
- **`align-items` vs `text-align`:** `align-items: center` centers the box, not the lines inside it. I wrote `text-align: center` once on the parent and let the children inherit it.
- **`box-sizing: border-box`:** Padding is included in `max-width`. I put the side padding on the outer section, so I can use the widths from Figma as they are.
- **Drawing a line with `::before`:** The line above the "01" / "02" circle is a pseudo-element.

```css
.order {
  position: relative;
}

.order::before {
  content: "";
  height: 80px;
  border-left: 1px solid var(--slate-300);
  position: absolute;
  top: -80px;
}
```

- **Background image with a color:** `background-size: cover` fills the box, and `background-blend-mode: multiply` mixes the cyan color with the photo.

### Continued development

- Check with DevTools more often. Many problems were easy to see there.
- Check color contrast on hover states.

### AI Collaboration

- I used Claude Code as a mentor. It reviewed my code after each step and gave me hints instead of answers.
- What didn't work well: its first hint (`<picture>`) did not fit this design. But trying it taught me how `<picture>` works.

## Author

- Frontend Mentor - [@naoki-takami0120](https://www.frontendmentor.io/profile/naoki-takami0120)
