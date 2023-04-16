---
title: Adding a background image using react inline styles
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To set a background image with React inline styles in Javascript, you can use the `backgroundImage` property with a URL value.
---

**Contents**

[TOC]

## Setting the Image

In React, you can use inline styles to set a background image. To do this, you need to create an object with a `backgroundImage` property, and assign it to the `style` attribute of the element you want to set the background image of.

```js
const elementStyle = {
  backgroundImage: `url(${imageUrl})`
};

<div style={elementStyle}>
  ...
</div>
```

## Setting the Image Position

By default, the background image will be positioned at the top left corner of the element. To change this, you can set the `backgroundPosition` property of the style object to the desired position.

```js
const elementStyle = {
  backgroundImage: `url(${imageUrl})`,
  backgroundPosition: 'center'
};

<div style={elementStyle}>
  ...
</div>
```

## Setting the Image Size

By default, the background image will be sized to fit the element. To change this, you can set the `backgroundSize` property of the style object to the desired size.

```js
const elementStyle = {
  backgroundImage: `url(${imageUrl})`,
  backgroundPosition: 'center',
  backgroundSize: 'cover'
};

<div style={elementStyle}>
  ...
</div>
```

## Setting the Image Repeat

By default, the background image will not be repeated. To change this, you can set the `backgroundRepeat` property of the style object to the desired repeat value.

```js
const elementStyle = {
  backgroundImage: `url(${imageUrl})`,
  backgroundPosition: 'center',
  backgroundSize: 'cover',
  backgroundRepeat: 'repeat'
};

<div style={elementStyle}>
  ...
</div>
```
