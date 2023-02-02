---
title: What is the best way to save data to html5 localstorage/sessionstorage?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Objects can be stored in localStorage/sessionStorage in Javascript by using the setItem() method.
---

**Contents**

[TOC]

## JSON Stringify

The most common way to store objects in localStorage/sessionStorage is to convert the object into a string using `JSON.stringify()`. This will allow us to store the object as a string in the localStorage/sessionStorage.

## Retrieving Objects

When we want to retrieve the object from localStorage/sessionStorage, we can use `JSON.parse()` to convert the string back into an object. This will allow us to access the object's properties and manipulate them as needed.

## Storing and Retrieving

To store an object in localStorage/sessionStorage, we use the following code:

```javascript
// Store an object in localStorage
localStorage.setItem('myObject', JSON.stringify(myObject));

// Retrieve an object from localStorage
var myObject = JSON.parse(localStorage.getItem('myObject'));
```

## Limitations

It is important to note that localStorage/sessionStorage can only store strings, so we must use `JSON.stringify()` and `JSON.parse()` to store and retrieve objects. Additionally, localStorage/sessionStorage has a maximum size limit, so we must be careful not to exceed this limit when storing objects.
