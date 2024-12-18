# The Paint Clone

The Paint Clone project is an interactive and customizable web-based drawing application inspired by classic desktop paint programs. It allows users to draw, erase, and customize their creations, leveraging modern web technologies like HTML5 Canvas, CSS, and JavaScript.

This project was developed as part of the course "JavaScript Web Projects: 20 Projects to Build Your Portfolio" by Zero To Mastery.

## Table of contents

- [The Paint Clone](#the-paint-clone)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

The Paint Clone provides a simple and intuitive interface for creating and saving drawings directly in the browser. It combines essential drawing features with additional customization options for a tailored experience.

### Screenshot

![](./screenshot.png)

### Links

- Live Site URL: [DT Code](https://paint-clone.dtcode.se/)

### Built with

- HTML5:
  - Canvas API for interactive drawing.
  - Semantic structure for toolbar and controls.
- CSS3:
  - Custom styling for tools and sliders.
  - Responsive design optimized for desktop use.
- JavaScript (ES6+):
  - Canvas drawing functionality.
  - Event-driven interactions.
  - Local storage management for saving and loading.

### What I learned

This project significantly improved my understanding of:
- HTML5 Canvas:
  - Drawing lines and managing canvas state.
  - Handling brush properties such as size, color, and erasing.
- Event Handling:
  - Managing mouse events for drawing and interaction.
  - Handling tool selection dynamically.
- Local Storage:
  - Persisting canvas drawings across sessions.
- Download Functionality:
  - Exporting canvas content as an image file.

The following snippet demonstrates how mouse movements are captured and translated into drawings on the canvas:

```js
canvas.addEventListener('mousemove', (event) => {
  if (isMouseDown) {
    const currentPosition = getMousePosition(event);
    context.lineTo(currentPosition.x, currentPosition.y);
    context.stroke();
    storeDrawn(
      currentPosition.x,
      currentPosition.y,
      currentSize,
      currentColor,
      isEraser
    );
  }
});
```

### Useful resources

- [MDN Web Docs: Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) - A comprehensive guide to working with the Canvas element.
- [MDN Web Docs: Local Storage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) - Helped in implementing save and load functionality.

## Author

- GitHub - [@dantvi](https://github.com/dantvi)
- LinkedIn - [@danieltving](https://www.linkedin.com/in/danieltving/)

## Acknowledgments

Special thanks to Zero To Mastery for their well-structured course, and to MDN Web Docs for their in-depth technical documentation that guided this project.
