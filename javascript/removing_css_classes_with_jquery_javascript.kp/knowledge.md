---
title: What is the best way to delete all css classes using jquery/javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: $(`.className`).removeClass();
---

**Contents**

[TOC]

## Solution 1:
Using a `for` loop to iterate over all elements in the DOM and removing all classes associated with them:

```javascript
var elements = document.getElementsByTagName('*');

for (var i = 0; i < elements.length; i++) {
    elements[i].className = '';
}
```

## Solution 2:
Using jQuery's `removeClass` method to remove all classes associated with all elements:

```javascript
$('*').removeClass();
```

## Solution 3:
Using the `querySelectorAll` method to select all elements in the DOM and then using the `classList` method to remove all classes associated with them:

```javascript
var elements = document.querySelectorAll('*');

for (var i = 0; i < elements.length; i++) {
    elements[i].classList.remove();
}
```

## Solution 4:
Using jQuery's `removeAttr` method to remove all classes associated with all elements:

```javascript
$('*').removeAttr('class');
```
