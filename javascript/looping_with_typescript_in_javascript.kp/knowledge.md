---
title: Iterating over a dictionary using typescript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To loop through a dictionary in JavaScript, you can use a for-in loop to iterate over the keys and access the associated values.
---

**Contents**

[TOC]

## Using for-in loop
The for-in loop is the most common way to loop through a dictionary in JavaScript. The syntax is as follows: 

```javascript
for (const key in object) {
   // do something with object[key]
}
```

Where `object` is the dictionary, and `key` is the key of the dictionary. For example, to loop through a dictionary called `myDict`:

```javascript
for (const key in myDict) {
   console.log(myDict[key]);
}
```

## Using for-of loop
The for-of loop is an ES6 feature that allows you to loop through an iterable object, such as an array or a dictionary. The syntax is as follows:

```javascript
for (const value of object) {
   // do something with value
}
```

Where `object` is the dictionary, and `value` is the value of the dictionary. For example, to loop through a dictionary called `myDict`:

```javascript
for (const value of myDict) {
   console.log(value);
}
```

## Using Object.keys()
The Object.keys() method returns an array of the keys of an object. This can be used to loop through a dictionary. The syntax is as follows:

```javascript
const keys = Object.keys(object);
for (const key of keys) {
   // do something with object[key]
}
```

Where `object` is the dictionary, and `key` is the key of the dictionary. For example, to loop through a dictionary called `myDict`:

```javascript
const keys = Object.keys(myDict);
for (const key of keys) {
   console.log(myDict[key]);
}
```

## Using Object.entries()
The Object.entries() method returns an array of the key-value pairs of an object. This can be used to loop through a dictionary. The syntax is as follows:

```javascript
const entries = Object.entries(object);
for (const [key, value] of entries) {
   // do something with key and value
}
```

Where `object` is the dictionary, `key` is the key of the dictionary, and `value` is the value of the dictionary. For example, to loop through a dictionary called `myDict`:

```javascript
const entries = Object.entries(myDict);
for (const [key, value] of entries) {
   console.log(key, value);
}
```
