---
title: What is the equivalent of jquery's document.createelement?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: In Javascript, the equivalent of jQuery`s document.createElement is document.createElement().
---

**Contents**

[TOC]

**1. Creating an Element**

To create an element using JavaScript, you can use the `document.createElement()` method. This method takes a single argument, which is the tag name of the element you want to create.

For example, to create a `<div>` element:

```javascript
var div = document.createElement('div');
```

**2. Adding Attributes**

Once you have created an element, you can add attributes to it using the `setAttribute()` method. This method takes two arguments: the attribute name and the attribute value.

For example, to add a `class` attribute with the value `container` to the `<div>` element above:

```javascript
div.setAttribute('class', 'container');
```

**3. Adding Content**

You can add content to the element by setting its `innerHTML` property. This property takes a string of HTML that will be rendered inside the element.

For example, to add a `<p>` element with some text inside the `<div>` element above:

```javascript
div.innerHTML = '<p>This is some content inside the div.</p>';
```

**4. Appending to the Document**

Finally, you can add the element to the document by appending it to an existing element using the `appendChild()` method. This method takes a single argument, which is the element you want to append.

For example, to append the `<div>` element to the `<body>` element:

```javascript
document.body.appendChild(div);
```
