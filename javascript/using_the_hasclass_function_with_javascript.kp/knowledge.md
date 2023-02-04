---
title: What does the 'hasclass' function do in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The `hasClass` function is a plain JavaScript function that checks if an element has a specified class name.
---

**Contents**

[TOC]

#### Definition

The `hasClass()` function is a JavaScript function that checks if a particular element has a specific class assigned to it. It returns a boolean value of true if the element has the specified class and false if it does not.

#### Syntax

The syntax for the `hasClass()` function is as follows:

```javascript
element.hasClass(className);
```

Where `element` is the DOM element and `className` is the name of the class to check for.

#### Example

The following example uses the `hasClass()` function to check if an element with the id of "myDiv" has the class "myClass":

```javascript
var myDiv = document.getElementById("myDiv");
if (myDiv.hasClass("myClass")) {
  // do something
}
```

#### Browser Support

The `hasClass()` function is supported by all modern browsers.
