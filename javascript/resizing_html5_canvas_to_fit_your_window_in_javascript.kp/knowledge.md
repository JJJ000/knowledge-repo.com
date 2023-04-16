---
title: Adjust the size of the html5 canvas to fit the window
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The canvas can be resized to fit the window by setting its width and height attributes to match the window`s innerWidth and innerHeight.
---

**Contents**

[TOC]

# Section 1: Get the Canvas Element

The first step is to get the canvas element from the DOM. This can be done using the `document.getElementById()` method.

```javascript
let canvas = document.getElementById("mycanvas");
```

# Section 2: Get the Window Dimensions

The next step is to get the window dimensions using the `window.innerWidth` and `window.innerHeight` properties.

```javascript
let windowWidth = window.innerWidth;
let windowHeight = window.innerHeight;
```

# Section 3: Set the Canvas Dimensions

The last step is to set the canvas dimensions to the window dimensions. This can be done using the `canvas.width` and `canvas.height` properties.

```javascript
canvas.width = windowWidth;
canvas.height = windowHeight;
```

# Section 4: Redraw the Canvas

Finally, to ensure that the canvas is correctly resized, it is necessary to redraw the canvas using the `context.drawImage()` method.

```javascript
let context = canvas.getContext("2d");
context.drawImage(canvas, 0, 0, canvas.width, canvas.height);
```
