---
title: How to erase the canvas for redrawing
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To clear the canvas for redrawing, use the canvas`s clearRect() method.
---

**Contents**

[TOC]

1. Getting the Canvas Element

In order to clear the canvas, you must first get the canvas element. This can be done by using the `getElementById()` method. This method takes in the `id` of the canvas element and returns the canvas element.


```
const canvas = document.getElementById('canvas');
```

2. Clearing the Canvas

Once you have the canvas element, you can then clear it by setting the width and height of the canvas. This can be done by setting the `width` and `height` attributes of the canvas element.

```
canvas.width = 500;
canvas.height = 500;
```

3. Redrawing the Canvas

Once the canvas is cleared, you can then redraw the canvas. This can be done by using the `drawImage()` method. This method takes in the image and draws it onto the canvas.

```
const img = new Image();
img.src = 'image.png';

ctx.drawImage(img, 0, 0);
```

4. Updating the Canvas

Finally, you can update the canvas by calling the `update()` method. This method takes in the new image and updates the canvas with the new image.

```
const newImg = new Image();
newImg.src = 'newImage.png';

ctx.update(newImg);
```
