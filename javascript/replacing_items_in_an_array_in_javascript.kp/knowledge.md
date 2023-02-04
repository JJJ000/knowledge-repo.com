---
title: What is the process for replacing an item in an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Array.splice() method to replace an item in an array.
---

**Contents**

[TOC]

##### Using the splice() Method
1. Use the `splice()` method to remove the item at the specified index.

```javascript
array.splice(index, 1);
```

2. Use the `splice()` method again to add the new item at the specified index.

```javascript
array.splice(index, 0, item);
```

##### Using the spread operator
1. Create a new array by removing the item at the specified index.

```javascript
let newArray = [...array.slice(0, index), ...array.slice(index + 1)];
```

2. Create a new array by adding the new item at the specified index.

```javascript
let newArray = [...array.slice(0, index), item, ...array.slice(index)];
```
