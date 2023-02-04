---
title: Find all values that appear more than once in an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Array.prototype.filter() method to filter out all values that have more than one occurrence in the array.
---

**Contents**

[TOC]

**Using For Loop**

```javascript
function getNonUniqueValues(arr) {
  const nonUniqueValues = [];

  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[i] === arr[j]) {
        nonUniqueValues.push(arr[i]);
      }
    }
  }

  return nonUniqueValues;
}
```

**Using Set**

```javascript
function getNonUniqueValues(arr) {
  const nonUniqueValues = [];
  const set = new Set();

  for (let i = 0; i < arr.length; i++) {
    if (set.has(arr[i])) {
      nonUniqueValues.push(arr[i]);
    } else {
      set.add(arr[i]);
    }
  }

  return nonUniqueValues;
}
```

**Using Filter**

```javascript
function getNonUniqueValues(arr) {
  return arr.filter((item, index) => arr.indexOf(item) !== index);
}
```

**Using Reduce**

```javascript
function getNonUniqueValues(arr) {
  return arr.reduce((acc, item) => {
    if (arr.indexOf(item) !== arr.lastIndexOf(item)) {
      acc.push(item);
    }
    return acc;
  }, []);
}
```
