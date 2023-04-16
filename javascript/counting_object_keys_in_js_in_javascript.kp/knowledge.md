---
title: What is the most effective way to count the number of keys/properties of an object in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The most efficient way to count the number of keys/properties of an object in JavaScript is to use the Object.keys() method.
---

**Contents**

[TOC]

**1. Using Object.keys()**

Object.keys() is a built-in method that returns an array of the object's own enumerable properties. This method takes an object as its parameter and returns an array of strings that represent the keys of the object.

To use Object.keys(), you can use the following syntax:

```javascript
Object.keys(objectName);
```

Once you have the array of keys, you can use the length property to get the number of keys in the object.

```javascript
Object.keys(objectName).length;
```

**2. Using a for...in loop**

A for...in loop is a built-in looping statement that allows you to iterate through the properties of an object. To use a for...in loop, you can use the following syntax:

```javascript
for (let key in objectName) {
  // code to be executed
}
```

Inside the loop, you can increment a counter variable each time the loop iterates. Once the loop is finished, the counter variable will hold the total number of keys in the object.

**3. Using Object.entries()**

Object.entries() is a built-in method that returns an array of the object's own enumerable property [key, value] pairs. This method takes an object as its parameter and returns an array of arrays that represent the key/value pairs of the object.

To use Object.entries(), you can use the following syntax:

```javascript
Object.entries(objectName);
```

Once you have the array of key/value pairs, you can use the length property to get the number of keys in the object.

```javascript
Object.entries(objectName).length;
```

**4. Using Object.getOwnPropertyNames()**

Object.getOwnPropertyNames() is a built-in method that returns an array of all properties (enumerable or not) found directly upon a given object. This method takes an object as its parameter and returns an array of strings that represent the properties of the object.

To use Object.getOwnPropertyNames(), you can use the following syntax:

```javascript
Object.getOwnPropertyNames(objectName);
```

Once you have the array of properties, you can use the length property to get the number of keys in the object.

```javascript
Object.getOwnPropertyNames(objectName).length;
```
