# Frontend Mentor - Profile card component solution

This is a solution to the [Profile card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/profile-card-component-cfArpWshJ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

- Build out the project to the designs provided

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/profile-card-8LKdvnyC4I](https://www.frontendmentor.io/solutions/profile-card-8LKdvnyC4I)
- Live Site URL: [https://iwanharyatno.github.com/fm-profile-card](https://iwanharyatno.github.com/fm-profile-card)

## My process

### Built with

- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

After I worked on this project, I've learned on how to hide the overflowing content of absolute positioned element, especially if the overflow occurs on right and bottom side of the viewport.

Here's how I do it.

First I set the possible overflowing content (which in this case, a pretty big image for background decoration) inside of an element.
```html
<div class="pattern-bottom">
  <img src="images/bg-pattern-bottom.svg" alt="Pattern Bottom">
</div>
```

And then I set the position of the outer class (`pattern-bottom`) as absolute, and place it where I needed.
```css
.pattern-bottom {
  position: absolute;
  z-index: -1;
  top: 50%;
  left: 50%;
}
```

And now for the fun part.  Here, I also set the right and the bottom property alongside the top and left property (so I set all of them simultaneously).
```css
.pattern-bottom {
  ...
  bottom: 0;
  right: 0;
  overflow: hidden;
}
```

And boom! It worked :)

### Useful resources

- [overflow - CSS - prevent absolute positioned element from overflowing body - Stack Overflow](https://stackoverflow.com/questions/9933092/css-prevent-absolute-positioned-element-from-overflowing-body) - This question really helps me on how I managed to hide the overflowing decoration component on the right and bottom side of the viewport.

## Author

- Website - [Iwan Haryatno](https://iwanharyatno.github.io)
- Frontend Mentor - [@iwanharyatno](https://www.frontendmentor.io/profile/iwanharyatno)
