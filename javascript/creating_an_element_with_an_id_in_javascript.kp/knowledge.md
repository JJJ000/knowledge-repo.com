---
title: What is the id of the element you are creating?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: CreateElement() is a method used to create an element with a specified ID in JavaScript.
---

**Contents**

[TOC]

#### Creating an Element

Creating an element with an id in Javascript is done using the `document.createElement` method. This method takes one parameter, which is the tag name of the element to be created. For example, to create a `<div>` element with an id of `myDiv`, the following code can be used:

```javascript
let myDiv = document.createElement('div');
myDiv.id = 'myDiv';
```

#### Adding the Element to the DOM

Once the element has been created, it can be added to the DOM by using the `document.appendChild` method. This method takes one parameter - the element to be added. For example, to add the `<div>` element created above to the DOM, the following code can be used:

```javascript
document.body.appendChild(myDiv);
```

#### Manipulating the Element

Once the element has been added to the DOM, it can be manipulated using the various methods available on the element. For example, to set the text content of the `<div>` element, the following code can be used:

```javascript
myDiv.textContent = 'Hello World!';
```

#### Styling the Element

The element can also be styled using the `style` property. For example, to set the background color of the `<div>` element, the following code can be used:

```javascript
myDiv.style.backgroundColor = 'red';
```
