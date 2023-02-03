---
title: What is the best way to save an array in localstorage?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the localStorage.setItem() method to store an array in localStorage.
---

**Contents**

[TOC]

## Step 1: Stringify the Array 
The first step is to convert the array into a string. This can be done with the `JSON.stringify()` method:

```javascript
var myArray = [1,2,3];
var arrayString = JSON.stringify(myArray);
```

## Step 2: Store the String in LocalStorage
Once the array is stored as a string, it can be stored in localStorage. This can be done with the `localStorage.setItem()` method:

```javascript
localStorage.setItem('myArray', arrayString);
```

## Step 3: Retrieve the String from LocalStorage
When you want to retrieve the array from localStorage, you can use the `localStorage.getItem()` method:

```javascript
var storedArrayString = localStorage.getItem('myArray');
```

## Step 4: Parse the String into an Array
Finally, the string can be parsed back into an array using the `JSON.parse()` method:

```javascript
var retrievedArray = JSON.parse(storedArrayString);
```
