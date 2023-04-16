---
title: Creating a binary large object (blob) from a base64 encoded string in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can create a BLOB from a Base64 string in JavaScript by using the atob() function.
---

**Contents**

[TOC]

### Creating a Blob

A Blob object can be created from a Base64 string using the `atob()` method to decode the Base64 string and the Blob constructor to create the Blob object.

### atob() Method

The `atob()` method is used to decode a Base64 encoded string. It takes a single argument which is the Base64 string to be decoded and returns the decoded string.

### Blob Constructor

The Blob constructor is used to create a new Blob object. It takes two arguments, an array of parts and an object containing the properties of the Blob. The array of parts should contain the decoded Base64 string from the `atob()` method.

### Example

Below is an example of how to create a Blob from a Base64 string in JavaScript:

```javascript
// Create a Base64 string
const base64String = 'SGVsbG8gV29ybGQ=';

// Decode the Base64 string using the atob() method
const decodedString = atob(base64String);

// Create the Blob object using the Blob constructor
const blob = new Blob([decodedString], {type: 'text/plain'});
```
