---
title: Adding an element to the start of a JavaScript array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To push an element at the beginning of an array, use the Array.unshift() method.
---

**Contents**

[TOC]

**Using the Array.prototype.unshift() Method**

The `Array.prototype.unshift()` method can be used to add one or more elements to the beginning of an array. The `unshift()` method returns the new length of the array.

**Syntax**

The syntax for using the `unshift()` method is as follows:

```
array.unshift(element1[, ...[, elementN]])
```

**Example**

The following example shows how to use the `unshift()` method to add an element to the beginning of an array:

```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");

// fruits is now ["Lemon", "Banana", "Orange", "Apple", "Mango"]
```

**Using the Spread Operator**

The spread operator (`...`) can also be used to add an element to the beginning of an array. The spread operator creates a shallow copy of the array and then adds the new element to the beginning of the copied array.

**Syntax**

The syntax for using the spread operator to add an element to the beginning of an array is as follows:

```
[element, ...array]
```

**Example**

The following example shows how to use the spread operator to add an element to the beginning of an array:

```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var newFruits = ["Lemon", ...fruits];

// newFruits is now ["Lemon", "Banana", "Orange", "Apple", "Mango"]
```
