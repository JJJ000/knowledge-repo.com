---
title: What is the most straightforward way to find the intersection of two arrays in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The simplest code for array intersection in JavaScript is to use the Array.prototype.filter() method.
---

**Contents**

[TOC]

### Section 1: Create a Set

In order to use the most efficient code for an array intersection, it is necessary to create a Set from the first array. A Set is a data structure that stores unique values.

```javascript
const setA = new Set(arrA);
```

### Section 2: Filter the Second Array

Once the Set is created, the second array can be filtered to only contain values that are also in the Set.

```javascript
const arrBFiltered = arrB.filter(x => setA.has(x));
```

### Section 3: Create the Intersection Array

Using the filtered array, the intersection array can be created by mapping the filtered array into a new array.

```javascript
const intersection = arrBFiltered.map(x => x);
```

### Section 4: Return the Intersection Array

Finally, the intersection array can be returned.

```javascript
return intersection;
```
