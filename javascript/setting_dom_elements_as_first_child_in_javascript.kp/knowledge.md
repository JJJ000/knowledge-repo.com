---
title: What is the process for making a dom element the first child?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the insertBefore() method to insert an element as the first child of a parent element.
---

**Contents**

[TOC]

## 1. Using appendChild

The `appendChild()` method can be used to set an element as the first child of a parent element. The syntax is as follows:

```javascript
parentElement.appendChild(element);
```

Where `parentElement` is the parent DOM element, and `element` is the DOM element to be set as the first child.

## 2. Using insertBefore

The `insertBefore()` method can also be used to set an element as the first child of a parent element. The syntax is as follows:

```javascript
parentElement.insertBefore(element, parentElement.firstChild);
```

Where `parentElement` is the parent DOM element, and `element` is the DOM element to be set as the first child.

## 3. Example

Let's consider the following HTML code:

```html
<div id="parent">
    <div id="child1"></div>
    <div id="child2"></div>
</div>
```

If we want to set the `<div id="child2">` element as the first child of the `<div id="parent">` element, we can use either of the following methods:

Using `appendChild()`:

```javascript
let parentElement = document.getElementById('parent');
let element = document.getElementById('child2');

parentElement.appendChild(element);
```

Using `insertBefore()`:

```javascript
let parentElement = document.getElementById('parent');
let element = document.getElementById('child2');

parentElement.insertBefore(element, parentElement.firstChild);
```

## 4. Output

After running the above code, the HTML code will be as follows:

```html
<div id="parent">
    <div id="child2"></div>
    <div id="child1"></div>
</div>
```
