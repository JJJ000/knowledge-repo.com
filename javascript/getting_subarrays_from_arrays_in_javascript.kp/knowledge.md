---
title: What is the best way to extract a portion of an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Array.slice() method to get a subarray from an array in Javascript.
---

**Contents**

[TOC]

1. Using the Slice Method
 
The slice() method can be used to get a subarray from an array. The slice() method takes two arguments; the start index, and the end index (exclusive). The start index is the index at which the subarray starts, and the end index is the index at which the subarray ends.

For example, if you wanted to get a subarray from an array that starts at index 2 and ends at index 5, you could use the following code:

```
let array = [1, 2, 3, 4, 5, 6, 7];
let subArray = array.slice(2, 5);
console.log(subArray); // [3, 4, 5]
```

2. Using the Splice Method

The splice() method can also be used to get a subarray from an array. The splice() method takes two arguments; the start index, and the number of elements to be removed from the array.

For example, if you wanted to get a subarray from an array that starts at index 2 and ends at index 5, you could use the following code:

```
let array = [1, 2, 3, 4, 5, 6, 7];
let subArray = array.splice(2, 3);
console.log(subArray); // [3, 4, 5]
```

3. Using the Array.from Method

The Array.from() method can also be used to get a subarray from an array. The Array.from() method takes two arguments; the array to be converted, and a map function (optional). The map function can be used to manipulate the elements of the array.

For example, if you wanted to get a subarray from an array that starts at index 2 and ends at index 5, you could use the following code:

```
let array = [1, 2, 3, 4, 5, 6, 7];
let subArray = Array.from(array, (val, index) => {
    if (index >=2 && index <= 5) {
        return val;
    }
});
console.log(subArray); // [3, 4, 5]
```

4. Using the Filter Method

The filter() method can also be used to get a subarray from an array. The filter() method takes a callback function as an argument, which is used to filter out elements from the array.

For example, if you wanted to get a subarray from an array that starts at index 2 and ends at index 5, you could use the following code:

```
let array = [1, 2, 3, 4, 5, 6, 7];
let subArray = array.filter((val, index) => {
    if (index >=2 && index <= 5) {
        return val;
    }
});
console.log(subArray); // [3, 4, 5]
```
