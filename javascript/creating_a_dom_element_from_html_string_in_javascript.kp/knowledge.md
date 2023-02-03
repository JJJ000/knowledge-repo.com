---
title: Constructing a fresh dom element from an html string with the help of built-in dom functions or prototype
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Using the built-in DOM method `createElement()` and `innerHTML`, a new DOM element can be created from an HTML string.
---

**Contents**

[TOC]

**Section 1: Using Built-in DOM Methods**

1. Create a new `div` element
```javascript
let newDiv = document.createElement('div');
```
2. Set the `innerHTML` property of the element to the HTML string
```javascript
newDiv.innerHTML = "<p>This is an example HTML string.</p>";
```
3. Append the element to the DOM
```javascript
document.body.appendChild(newDiv);
```

**Section 2: Using Prototype**

1. Create a new `div` element
```javascript
let newDiv = new Element('div');
```
2. Set the `innerHTML` property of the element to the HTML string
```javascript
newDiv.update("<p>This is an example HTML string.</p>");
```
3. Append the element to the DOM
```javascript
document.body.appendChild(newDiv);
```
