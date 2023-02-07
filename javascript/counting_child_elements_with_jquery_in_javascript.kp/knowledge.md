---
title: Find the number of child elements using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery can count child elements using the .children() method.
---

**Contents**

[TOC]

#### Using jQuery

To count the number of child elements of a given element using jQuery, you can use the `length` property of the result of the `children` method:

```js
var numChildren = $('#elementId').children().length;
```

#### Using JavaScript

To count the number of child elements of a given element using JavaScript, you can use the `children` property of the element and the `length` property of the result:

```js
var numChildren = document.getElementById('elementId').children.length;
```

#### Using a For Loop

You can also count the number of child elements of a given element using a for loop:

```js
var element = document.getElementById('elementId');
var numChildren = 0;
for (var i = 0; i < element.children.length; i++) {
    numChildren++;
}
```

#### Using a While Loop

Alternatively, you can count the number of child elements of a given element using a while loop:

```js
var element = document.getElementById('elementId');
var numChildren = 0;
var i = 0;
while (i < element.children.length) {
    numChildren++;
    i++;
}
```
