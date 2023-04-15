---
title: What is the syntax to modify an element's class using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can change an element`s class with JavaScript by using the element`s `className` property.
---

**Contents**

[TOC]

### Using getElementsByClassName()

The `getElementsByClassName()` method can be used to select an element by its class name. The method returns an array-like object of all child elements which have all of the given class names.

Once the element has been selected, the `className` property can be used to change the class of the element.

```javascript
// Select element by class name
var element = document.getElementsByClassName('class-name')[0];

// Change the class
element.className = 'new-class-name';
```

### Using querySelector()

The `querySelector()` method can also be used to select an element by its class name. The method returns the first element within the document that matches the specified selector.

Once the element has been selected, the `className` property can be used to change the class of the element.

```javascript
// Select element by class name
var element = document.querySelector('.class-name');

// Change the class
element.className = 'new-class-name';
```
