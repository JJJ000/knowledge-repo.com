---
title: Arrange the elements of the array in alphabetical order based on the first name using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Array.sort(function(a, b) { return a.firstname.localeCompare(b.firstname); });
---

**Contents**

[TOC]

### Step 1: Create an Array of Objects

We can create an array of objects that contain firstname and lastname properties.

```javascript
const names = [
  { firstname: 'John', lastname: 'Doe' },
  { firstname: 'Jane', lastname: 'Smith' },
  { firstname: 'Adam', lastname: 'Johnson' }
];
```

### Step 2: Sort the Array

We can use the `Array.prototype.sort()` method to sort the array. The `sort()` method takes a compare function as an argument. This compare function will determine how the array is sorted.

```javascript
names.sort((a, b) => {
  if (a.firstname < b.firstname) {
    return -1;
  }
  if (a.firstname > b.firstname) {
    return 1;
  }
  return 0;
});
```

### Step 3: Log the Sorted Array

We can log the sorted array to the console to see the result.

```javascript
console.log(names);
```

### Step 4: Output

The output will be an array of objects sorted alphabetically by firstname.

```javascript
[
  { firstname: 'Adam', lastname: 'Johnson' },
  { firstname: 'Jane', lastname: 'Smith' },
  { firstname: 'John', lastname: 'Doe' }
]
```
