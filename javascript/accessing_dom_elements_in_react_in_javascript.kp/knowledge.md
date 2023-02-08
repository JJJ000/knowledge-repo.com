---
title: What is the method for retrieving a dom element in react? what is the react equivalent of document.getelementbyid()?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: In React, the equivalent of document.getElementById() is React`s useRef() hook, which can be used to access a DOM element.
---

**Contents**

[TOC]

1. Accessing DOM Elements in React

In React, the DOM elements are accessed using the `ref` attribute. This attribute is used to create a reference to the DOM element and can be used to access the element's properties and methods.

2. Creating a Ref

To create a `ref`, you must first assign a callback function to the `ref` attribute of the element. This callback function will be called with the DOM element as its argument when the component is mounted.

For example, if you have a `<div>` element with the `id` of "myDiv", you would create a ref like this:

```js
<div ref={(el) => this.myDiv = el} id="myDiv">
  ...
</div>
```

3. Accessing the DOM Element

Once you have created the ref, you can access the DOM element by accessing the `myDiv` property of the component. For example, to get the element's `innerHTML` you would do this:

```js
const innerHTML = this.myDiv.innerHTML;
```

4. Equivalent of document.getElementById()

The equivalent of `document.getElementById()` in React is the `ReactDOM.findDOMNode()` method. This method takes a ref as its argument and returns the corresponding DOM element:

```js
const element = ReactDOM.findDOMNode(this.myDiv);
```
