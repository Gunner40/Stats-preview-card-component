# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

My task was to build out this card component and get it looking as close to the design as possible.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./Screenshot-stats-preview-card-component.png)

### Links

- Solution URL: https://github.com/Gunner40/Stats-preview-card-component
- Live Site URL: https://gunner40.github.io/Stats-preview-card-component/

## My process

Study the design and formulate a plan for how to approach the HTML and CSS.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

Used a picture element in the HTML because the image source changed depending on screen size.
Used an 'after' element to overlay a color with an opacity of 0.5 over the card image.

Also on mobile screens the component was taller than the height of the viewport. So on review, and after being pointed out by "Aaron Varga", I changed the height of the main element from "height: 100vh" to "min-height: 100vh. This fixed the issue. Aaron also sugested adding some padding-block to the main element so it would not hug the top and bottom of the screen on mobile devices. 

```html
<picture>
  <source
    media="(min-width:1000px)"
    srcset="./images/image-header-desktop.jpg"
  />
  <img
    src="./images/image-header-mobile.jpg"
    alt="office workers on laptops smiling"
  />
</picture>
```

```css
.card__image::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: var(--primary-accent);
  opacity: 0.5;
  z-index: 1;
}

main {
  min-height: 100vh;
  padding-block: 5em;
}
```

## Author

- Paul Ryan
- Frontend Mentor - [@Gunner40](https://www.frontendmentor.io/profile/Gunner40)
