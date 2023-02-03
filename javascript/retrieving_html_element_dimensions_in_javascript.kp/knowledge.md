---
title: What is the actual width and height of an html element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the `offsetWidth` and `offsetHeight` properties of the element to get its actual width and height in Javascript.
---

**Contents**

[TOC]

## Get Element

The first step is to get the HTML element you are interested in. This can be done using the `document.getElementById()` method. This method takes one argument, which is the `id` of the element you want to retrieve. 

## Get Width and Height

Once you have the element, you can use the `offsetWidth` and `offsetHeight` properties to get the element's actual width and height. These properties return the element's width and height, including any padding and border sizes.

## Get Computed Style

Alternatively, you can use the `getComputedStyle()` method to get the element's width and height. This method takes one argument, which is the element you want to retrieve the style for. It returns an object containing the element's computed style. You can then access the `width` and `height` properties to get the element's actual width and height.

## Get Client Rect

Finally, you can use the `getBoundingClientRect()` method to get the element's width and height. This method returns an object containing the element's size and position relative to the viewport. You can then access the `width` and `height` properties to get the element's actual width and height.
