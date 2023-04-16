---
title: What is the most efficient way to access form data using javascript/jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can get form data with JavaScript/jQuery by using the jQuery .serialize() method.
---

**Contents**

[TOC]

1. Using the `FormData` Object
--------------------------------
The `FormData` object lets you easily construct a set of key/value pairs representing form fields and their values, which can then be easily sent using the `XMLHttpRequest.send()` method.

To get form data using the `FormData` object:

1. Create a `FormData` object by passing a `<form>` element to the `FormData` constructor.
2. Iterate over the `FormData` object's entries, and access the data using the `name` and `value` properties.

Example:

```javascript
// Get the form element
const form = document.querySelector('form');

// Create a FormData object
const formData = new FormData(form);

// Iterate over the FormData object's entries
for (let entry of formData.entries()) {
   console.log(entry[0] + ', ' + entry[1]);
}
```

2. Using the `.serialize()` Method
---------------------------------
The `.serialize()` method of the jQuery library can be used to easily get form data. It serializes the form data into a URL-encoded string.

To get form data using the `.serialize()` method:

1. Select the form element using a jQuery selector.
2. Call the `.serialize()` method on the selected element.

Example:

```javascript
// Get the form element
const form = $('form');

// Get the form data as a URL-encoded string
const formData = form.serialize();

// Log the form data
console.log(formData);
```
