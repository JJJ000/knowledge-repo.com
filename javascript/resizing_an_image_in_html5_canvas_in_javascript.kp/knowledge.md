---
title: Changing the dimensions of an image in an html5 canvas
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To resize an image in an HTML5 canvas in Javascript, use the canvas`s drawImage() method with the desired width and height parameters.
---

**Contents**

[TOC]

#### Resizing an Image

1. Create a new canvas element and set its width and height to the desired size.

```js
var canvas = document.createElement('canvas');
canvas.width = newWidth;
canvas.height = newHeight;
```

2. Create an image object and set its source to the desired image.

```js
var image = new Image();
image.src = 'image.jpg';
```

3. Draw the image onto the canvas.

```js
var ctx = canvas.getContext('2d');
ctx.drawImage(image, 0, 0, newWidth, newHeight);
```

4. Get the data URL of the resized image.

```js
var resizedImageDataURL = canvas.toDataURL();
```
