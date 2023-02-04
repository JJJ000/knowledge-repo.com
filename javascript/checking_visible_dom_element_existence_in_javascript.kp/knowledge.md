---
title: Is there a way to determine if a particular element is present in the visible web page?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `document.querySelector()` method to check if an element exists in the visible DOM.
---

**Contents**

[TOC]

## Option 1: Using `document.querySelector()` 

The `document.querySelector()` method can be used to check if an element exists in the visible DOM. This method takes a CSS selector as an argument and returns the first element that matches the selector, or `null` if no elements match.

For example, to check if an element with the class `my-class` exists in the DOM, the following code can be used:

```javascript
let myElement = document.querySelector('.my-class');
if (myElement !== null) {
  // Element exists in the DOM
}
```

## Option 2: Using `document.getElementById()` 

The `document.getElementById()` method can also be used to check if an element exists in the visible DOM. This method takes an element's `id` attribute as an argument and returns the element that has that `id`, or `null` if no elements match.

For example, to check if an element with the `id` of `my-id` exists in the DOM, the following code can be used:

```javascript
let myElement = document.getElementById('my-id');
if (myElement !== null) {
  // Element exists in the DOM
}
```
