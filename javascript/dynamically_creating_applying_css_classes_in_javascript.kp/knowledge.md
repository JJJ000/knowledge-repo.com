---
title: How can I generate a css class within JavaScript and apply it?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can dynamically create a CSS class in JavaScript using the Element.classList.add() method and apply it to an element using the Element.classList.toggle() method.
---

**Contents**

[TOC]

## Creating CSS Class

CSS classes can be dynamically created in JavaScript using the `document.createElement()` method. This method takes two parameters; the first is the element type, and the second is an object containing any attributes that need to be set on the element.

To create a class, the element type should be `style`, and the attributes should include the `type` attribute set to `text/css` and the `innerText` attribute set to the CSS code defining the class.

For example, to create a class called `.example` that sets the font size to `14px`, the code would be:

```javascript
let cssClass = document.createElement("style");
cssClass.type = "text/css";
cssClass.innerText = ".example { font-size: 14px; }";
```

## Applying CSS Class

Once a CSS class has been created, it can be applied to an element using the `className` property. This property takes a string of space-separated class names, so multiple classes can be applied to an element at once.

For example, to apply the `.example` class to an element with the ID `exampleElement`, the code would be:

```javascript
let element = document.getElementById("exampleElement");
element.className = "example";
```

It is also possible to apply a CSS class to an element using the `classList` property. This property takes an array of class names, so multiple classes can be applied to an element at once.

For example, to apply the `.example` class to an element with the ID `exampleElement`, the code would be:

```javascript
let element = document.getElementById("exampleElement");
element.classList = ["example"];
```
