---
title: Display the contents of a div
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To print the contents of a DIV in Javascript, use the innerHTML property.
---

**Contents**

[TOC]

### Using `innerHTML`

The `innerHTML` property can be used to print the contents of a `div` element.

```js
var myDiv = document.getElementById("myDiv");
console.log(myDiv.innerHTML);
```

### Using `outerHTML`

The `outerHTML` property can be used to print the contents of a `div` element, including the `div` tag itself.

```js
var myDiv = document.getElementById("myDiv");
console.log(myDiv.outerHTML);
```

### Using `textContent`

The `textContent` property can be used to print the contents of a `div` element, including the text content but not the HTML tags.

```js
var myDiv = document.getElementById("myDiv");
console.log(myDiv.textContent);
```

### Using `innerText`

The `innerText` property can be used to print the contents of a `div` element, including the text content but not the HTML tags.

```js
var myDiv = document.getElementById("myDiv");
console.log(myDiv.innerText);
```
