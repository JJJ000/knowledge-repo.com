---
title: What is the syntax to add an element to a JavaScript array at a specific index?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the Array.splice() method to insert an item into an array at a specific index.
---

**Contents**

[TOC]

### Using Splice

The splice() method can be used to add elements to an array at a specified index.

Syntax:

```
array.splice(index, 0, item);
```

Example:

```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");

// fruits will be ["Banana", "Orange", "Lemon", "Kiwi", "Apple", "Mango"]
```

### Using Spread Operator

The spread operator (...) can also be used to add elements to an array at a specified index.

Syntax:

```
array = [...array.slice(0, index), item, ...array.slice(index)];
```

Example:

```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits = [...fruits.slice(0, 2), "Lemon", "Kiwi", ...fruits.slice(2)];

// fruits will be ["Banana", "Orange", "Lemon", "Kiwi", "Apple", "Mango"]
```
