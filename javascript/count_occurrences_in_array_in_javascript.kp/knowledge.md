---
title: Calculating the number of times each element appears in an array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The frequency of array elements in Javascript can be counted by using the Array.prototype.reduce() method.
---

**Contents**

[TOC]

##### Using for Loop

The following example uses a for loop to count the occurrences of each element in an array:

```javascript
var arr = [1, 2, 3, 4, 5, 4, 3, 2, 1];

var count = {};

for (var i = 0; i < arr.length; i++) {
  var num = arr[i];
  count[num] = count[num] ? count[num] + 1 : 1;
}

console.log(count); // {1: 2, 2: 2, 3: 2, 4: 2, 5: 1}
```

##### Using Reduce

The following example uses the reduce() method to count the occurrences of each element in an array:

```javascript
var arr = [1, 2, 3, 4, 5, 4, 3, 2, 1];

var count = arr.reduce(function(acc, curr) {
  if (typeof acc[curr] == 'undefined') {
    acc[curr] = 1;
  } else {
    acc[curr] += 1;
  }

  return acc;
}, {});

console.log(count); // {1: 2, 2: 2, 3: 2, 4: 2, 5: 1}
```

##### Using Map

The following example uses the map() method to count the occurrences of each element in an array:

```javascript
var arr = [1, 2, 3, 4, 5, 4, 3, 2, 1];

var count = arr.map(function(num) {
  return {
    num: num,
    count: arr.filter(function(n) {
      return n === num;
    }).length
  };
});

console.log(count); // [{num: 1, count: 2}, {num: 2, count: 2}, {num: 3, count: 2}, {num: 4, count: 2}, {num: 5, count: 1}]
```

##### Using Set

The following example uses a Set object to count the occurrences of each element in an array:

```javascript
var arr = [1, 2, 3, 4, 5, 4, 3, 2, 1];

var count = new Set(arr);

count.forEach(function(num) {
  console.log(num + ': ' + arr.filter(function(n) {
    return n === num;
  }).length);
});

// 1: 2
// 2: 2
// 3: 2
// 4: 2
// 5: 1
```
