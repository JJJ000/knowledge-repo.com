---
title: What is the syntax for retrieving the value of a text input field using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the `.value` property of the input element to get the value of the text input field.
---

**Contents**

[TOC]

1. Get Element by ID

The easiest way to get the value of a text input field is by using the `getElementById()` method. This method takes a single argument, the ID of the element you want to get.

```javascript
// Get the value of an input field with ID "textInput"
let textInputValue = document.getElementById("textInput").value;
```

2. Get Element by Class

If you want to get the value of multiple text input fields with the same class, you can use the `getElementsByClassName()` method. This method takes a single argument, the class of the elements you want to get.

```javascript
// Get the values of all input fields with class "textInput"
let textInputValues = document.getElementsByClassName("textInput");

// Loop through each element and get its value
let values = [];
for (let i = 0; i < textInputValues.length; i++) {
  values.push(textInputValues[i].value);
}
```

3. Get Element by Tag

If you want to get the value of all text input fields on the page, you can use the `getElementsByTagName()` method. This method takes a single argument, the tag of the elements you want to get.

```javascript
// Get the values of all input fields with tag "input"
let textInputValues = document.getElementsByTagName("input");

// Loop through each element and get its value
let values = [];
for (let i = 0; i < textInputValues.length; i++) {
  if (textInputValues[i].type === "text") {
    values.push(textInputValues[i].value);
  }
}
```

4. Query Selector

Finally, if you want to be more specific in the elements you want to get, you can use the `querySelector()` or `querySelectorAll()` methods. These methods take a single argument, a CSS selector that specifies the elements you want to get.

```javascript
// Get the values of all input fields with class "textInput"
let textInputValues = document.querySelectorAll(".textInput");

// Loop through each element and get its value
let values = [];
for (let i = 0; i < textInputValues.length; i++) {
  values.push(textInputValues[i].value);
}
```
