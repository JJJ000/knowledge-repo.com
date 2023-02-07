---
title: Looping through the output of getelementsbyclassname with array.foreach
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Array.forEach can be used to iterate over the result of getElementsByClassName, allowing the user to perform a specific action on each element.
---

**Contents**

[TOC]

**Section 1: Introduction**

The getElementsByClassName() method is a powerful way to select elements in the DOM (Document Object Model) by class name. It returns a NodeList of elements with the given class name. This NodeList can then be iterated over using the Array.forEach() method, which allows us to execute a function for each element in the NodeList.

**Section 2: Using Array.forEach()**

Using Array.forEach() to iterate over the NodeList returned by getElementsByClassName() is fairly straightforward. The following example shows how to do this:

```javascript
// Get a NodeList of elements with the class "example"
let elements = document.getElementsByClassName('example');

// Iterate over the NodeList
elements.forEach(function(element) {
  // Do something with each element
  console.log(element);
});
```

**Section 3: Using Arrow Functions**

The example above uses a regular function expression to define the callback for the forEach() method. However, arrow functions can also be used, as shown in the following example:

```javascript
// Get a NodeList of elements with the class "example"
let elements = document.getElementsByClassName('example');

// Iterate over the NodeList
elements.forEach(element => {
  // Do something with each element
  console.log(element);
});
```

**Section 4: Conclusion**

Iterating over the NodeList returned by getElementsByClassName() using Array.forEach() is a simple and effective way to work with multiple elements in the DOM. It is also possible to use arrow functions to define the callback for the forEach() method, which can help to make the code more concise.
