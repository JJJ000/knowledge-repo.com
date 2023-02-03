---
title: Move to the bottom of the div?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the element`s scrollTop property to scroll to the bottom of the div.
---

**Contents**

[TOC]

1. Get the Height of the Div 

2. Set the Scroll Position 

3. Scroll to the Bottom of the Div 

4. Example Code 

## 1. Get the Height of the Div 

The first step to scroll to the bottom of a div is to get the height of the div. This can be done using the `offsetHeight` property of the div element. This will return the height of the div in pixels. 

## 2. Set the Scroll Position 

Once we have the height of the div, we can set the scroll position of the div. This is done using the `scrollTop` property of the div element. We set the `scrollTop` to the height of the div. This will set the scroll position to the bottom of the div. 

## 3. Scroll to the Bottom of the Div 

Once the scroll position is set, we can use the `scrollTo()` method to scroll the div to the bottom. The `scrollTo()` method takes two parameters, the x coordinate and the y coordinate. We set the x coordinate to `0` and the y coordinate to the height of the div. This will scroll the div to the bottom. 

## 4. Example Code 

The following code snippet shows how to scroll to the bottom of a div using Javascript. 

```javascript
// Get the div element
let divElement = document.getElementById('myDiv');

// Get the height of the div
let divHeight = divElement.offsetHeight;

// Set the scroll position to the bottom of the div
divElement.scrollTop = divHeight;

// Scroll to the bottom of the div
divElement.scrollTo(0, divHeight);
```
