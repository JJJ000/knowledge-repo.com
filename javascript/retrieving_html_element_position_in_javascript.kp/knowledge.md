---
title: Find the x and y coordinates of an html element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The position (X,Y) of an HTML element can be retrieved using the element`s getBoundingClientRect() method.
---

**Contents**

[TOC]

## 1. Get the HTML Element

First, we need to get the HTML element that we want to retrieve the position of. This can be done with the `document.querySelector()` method.

```js
const element = document.querySelector('#myElement');
```

## 2. Get the Element's Position

Next, we need to get the element's position. This can be done using the `getBoundingClientRect()` method.

```js
const rect = element.getBoundingClientRect();
```

## 3. Get the X and Y Position

Finally, we need to get the X and Y position of the element. This can be done by accessing the `left` and `top` properties of the `rect` object.

```js
const x = rect.left;
const y = rect.top;
```

## 4. Output the Position

We can now output the X and Y position of the element.

```js
console.log(`Element's position is (${x}, ${y})`);
```
