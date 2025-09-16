# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

I did this project to sharpen my HTML and CSS skills. I hoped this project could be a learning experience and review the mistakes i made.

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![Screenshot.png](./Screenshots%20-%20Frontend%20Mentor%20-%20Blog%20preview%20card.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- [live site URL](https://heromunchen.github.io/frontend-mentor-practice-blogpreview/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid

### What I learned

### Tabindex
I learned how to use tabindex to make an element focusable if the user press tab. I used profile picture as the element that can be focused.

```html
<div class="profile">
  <img src="./assets/images/image-avatar.webp" alt="image-avatar" class="profile-picture"   tabindex="0">

  <p class="profile-name">
    Greg Hooper
  </p>
</div>
```

### Center a div
I learned a better way to center a div using the body as a grid and place-self to put the article card in the middle.

```css
body {
  background-color: hsl(47, 88%, 63%);
  font-family: 'Figtree';

  display: grid;
  grid-template-rows: 1fr auto;
  height: 100vh;
  margin: 0;
}

.article-card {
  background-color: white;
  padding: 13px 13px 10px 13px;
  border-radius: 10px;
  border-style: solid;
  border-width: 1px;
  box-shadow: 5px 5px 0 rgba(0, 0, 0, 1);
  transition: all 0.5s ease;

  display: flex;
  width: fit-content;
  flex-direction: column;
  justify-content: center;
  place-self: center;
}
```

### Simple hover and focus animation

I learned how to make a simple animation using transform to make the element bigger when hovered and glow. The same thing is done with profile picture when focused or hovered.

```css
.article-card:hover {
  transform: scale(1.05);
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
  border: none;
}

.profile-picture:focus, .profile-picture:hover {
  transform: scale(1.2);
  box-shadow: 0 0 10px rgba(0, 0, 0, 1);
  outline: none;
  cursor: pointer;
}
```

### Continued development

I am still not sure how figtree works and if used or ran correctly. I'll continue learn about figtree and use it correctly.

```css
@font-face {
  font-family: 'Figtree';
  src: url('./assets/fonts/Figtree-Italic-VariableFont_wght.ttf') format('truetype');
  font-weight: 100 900;
  font-style: italic;
}

@font-face {
  font-family: 'Figtree';
  src: url('./assets/fonts/Figtree-VariableFont_wght.ttf') format('truetype');
  font-weight: 100 900;
  font-style: normal;
}

@font-face {
  font-family: 'Figtree';
  src: url('./assets/fonts/static/Figtree-ExtraBold.ttf') format('truetype');
  font-weight: 800;
  font-style: normal;
}

@font-face {
  font-family: 'Figtree';
  src: url('./assets/fonts/static/Figtree-Medium.ttf') format('truetype');
  font-weight: 500;
  font-style: normal;
}
```

### Useful resources

- [Prismic](https://prismic.io/blog/css-hover-effects) - This helped me for giving inspiration on css hover and focus effects. I really liked this animation and will use it going forward.

## Author

- Frontend Mentor - [@Heromunchen](https://www.frontendmentor.io/profile/Heromunchen)