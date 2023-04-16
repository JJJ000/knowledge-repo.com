---
title: What is the method for determining if a value is present at a specific index in a JavaScript array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the array`s index notation (e.g. array[index]) to check if the value at the given index exists.
---

**Contents**

[TOC]

1. Using the `length` Property

To check if a value exists at a certain array index in JavaScript, you can use the `length` property of the array. This property returns the number of elements in the array, so if the index is greater than or equal to the length of the array, then the value at that index does not exist.

For example, consider the following array:

```javascript
const array = [1, 2, 3, 4];
```

To check if a value exists at index 3, you can use the `length` property as follows:

```javascript
if (array.length > 3) {
    // value exists at index 3
} else {
    // value does not exist at index 3
}
```

2. Using the `in` Operator

Another way to check if a value exists at a certain array index in JavaScript is to use the `in` operator. This operator returns `true` if the specified property is in the specified object, or `false` if not.

For example, consider the same array as before:

```javascript
const array = [1, 2, 3, 4];
```

To check if a value exists at index 3, you can use the `in` operator as follows:

```javascript
if (3 in array) {
    // value exists at index 3
} else {
    // value does not exist at index 3
}
```

3. Using the `indexOf()` Method

Another way to check if a value exists at a certain array index in JavaScript is to use the `indexOf()` method. This method returns the first index at which a given element can be found in the array, or -1 if it is not present.

For example, consider the same array as before:

```javascript
const array = [1, 2, 3, 4];
```

To check if a value exists at index 3, you can use the `indexOf()` method as follows:

```javascript
if (array.indexOf(3) > -1) {
    // value exists at index 3
} else {
    // value does not exist at index 3
}
```

4. Using the `includes()` Method

The last way to check if a value exists at a certain array index in JavaScript is to use the `includes()` method. This method returns `true` if the array includes the specified element, or `false` if not.

For example, consider the same array as before:

```javascript
const array = [1, 2, 3, 4];
```

To check if a value exists at index 3, you can use the `includes()` method as follows:

```javascript
if (array.includes(3)) {
    // value exists at index 3
} else {
    // value does not exist at index 3
}
```
