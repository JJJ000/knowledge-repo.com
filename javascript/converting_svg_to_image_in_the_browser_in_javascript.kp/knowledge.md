---
title: Transform an svg file into an image format (such as jpeg or png) in the web browser
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The svg.js library can be used to convert an SVG to an image (JPEG, PNG, etc.) in the browser using Javascript.
---

**Contents**

[TOC]

## Section 1: Prerequisites 

In order to convert SVG to an image in the browser in Javascript, there are a few prerequisites that must be met. First, the browser must support the HTML5 canvas element. Second, the SVG must be loaded in the browser, either from an external source or from an inline SVG element.

## Section 2: Converting SVG to Image

Once the prerequisites have been met, the SVG can be converted to an image by using the `canvas.toDataURL()` method. This method takes the SVG and converts it to a base64 encoded data URL that can be used to render an image in the browser.

## Section 3: Rendering the Image

Once the SVG has been converted to a data URL, it can be rendered in the browser by creating an image element with the data URL as its source. This can be done with the following code:

```
var image = new Image();
image.src = dataURL;
document.body.appendChild(image);
```

## Section 4: Outputting the Image

Once the image has been rendered in the browser, it can be output in a variety of formats, including JPEG, PNG, and others. This can be done by using the `canvas.toBlob()` method, which takes the image data and converts it to a blob that can be saved to the user's computer.
