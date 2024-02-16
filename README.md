# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [Code](https://github.com/phangtono/NFT-preview-card-component)
- Live Site URL: [Live Site URL](https://roaring-sawine-0e6002.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- CSS Grid
- Mobile-first workflow

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

I use background to display image-equilibrium.jpg, for background color (:after) and svg normal condition display:none, once hovered, display:block

```css
.card-image{
    background: var(--clr-primary-cyan) url('images/image-equilibrium.jpg');
    background-size:cover;
    width: 100%;
    aspect-ratio: 1;
    border-radius: var(--gap);
    
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    position: relative;
}

.card-image svg{
    display: none;
}

.card-image::after{
    position: absolute;
    content: '';
    width: 100%;
    aspect-ratio: 1;
    opacity: .4;
    background-color: var(--clr-primary-cyan);
    display: none;
    border-radius: var(--gap);
}

.card-image:hover svg{
    display: block;
    z-index: 1;
}

.card-image:hover::after{
    display: block;
}

```