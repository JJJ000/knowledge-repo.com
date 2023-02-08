---
title: Comparing JavaScript array splice and slice
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Array splice modifies the original array by removing and/or replacing elements, while Array slice returns a shallow copy of a portion of an array without modifying the original array.
---

**Contents**

[TOC]

### Splice
Splice is a method used to modify an array by removing or adding elements. It modifies the original array and returns the removed elements in a new array.

### Syntax
array.splice(startIndex[, deleteCount[, item1[, item2[, ...]]]])

### Parameters
- startIndex: The index at which to start changing the array.
- deleteCount: The number of elements to remove. If deleteCount is omitted, or if its value is equal to or larger than array.length - start, then all elements from start through the end of the array will be deleted.
- item1, item2, ...: The elements to add to the array, beginning from startIndex. If you don't specify any elements, splice() will only remove elements from the array.

### Slice
Slice is a method used to copy a part of an array into a new array. It does not modify the original array and returns the selected elements in a new array.

### Syntax
array.slice(startIndex[, endIndex])

### Parameters
- startIndex: The index at which to start the selection. If negative, it will begin that many elements from the end of the array.
- endIndex: The index at which to end the selection. If negative, it will end that many elements from the end of the array. If omitted, all elements from the start index to the end of the array will be selected.
