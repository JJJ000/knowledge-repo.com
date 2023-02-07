---
title: Organize a collection of objects based on a single date-related key
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the Array.prototype.sort() method to sort an array of objects by a single key with a date value.
---

**Contents**

[TOC]

## Solution 1:
Using the `Array.prototype.sort()` method:

```javascript
const sortedArray = arrayOfObjects.sort((a, b) => {
  return new Date(a.date) - new Date(b.date);
});
```

## Solution 2:
Using the `Array.prototype.sort()` method with a custom compare function:

```javascript
function compareDates(a, b) {
  const dateA = new Date(a.date);
  const dateB = new Date(b.date);

  let comparison = 0;
  if (dateA > dateB) {
    comparison = 1;
  } else if (dateA < dateB) {
    comparison = -1;
  }
  return comparison;
}

const sortedArray = arrayOfObjects.sort(compareDates);
```

## Solution 3:
Using the `Array.prototype.reduce()` method:

```javascript
const sortedArray = arrayOfObjects.reduce((acc, curr) => {
  const date = new Date(curr.date);
  const index = acc.findIndex(item => new Date(item.date) >= date);
  if (index === -1) {
    acc.push(curr);
  } else {
    acc.splice(index, 0, curr);
  }
  return acc;
}, []);
```

## Solution 4:
Using the `Array.prototype.map()` and `Array.prototype.sort()` methods:

```javascript
const sortedArray = arrayOfObjects
  .map(item => ({ ...item, sortDate: new Date(item.date) }))
  .sort((a, b) => a.sortDate - b.sortDate)
  .map(item => {
    const { sortDate, ...rest } = item;
    return rest;
  });
```
