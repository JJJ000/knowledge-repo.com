---
title: What is the best way to take out an element from an array based on its value?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.filter() method to remove an item from an array by its value.
---

**Contents**

[TOC]

##Using the splice() Method

The `splice()` method can be used to remove an item from an array by value. The `splice()` method takes two parameters: the index at which to start removing items, and the number of items to remove.

For example, if you have an array `var arr = [1,2,3,4,5]` and you want to remove the item with value `3`, you would use the `splice()` method like this: 

```
arr.splice(2,1);
```

This will remove the item at index 2 (which has value `3`) and only remove one item. The result will be an array with four items: `[1,2,4,5]`.

##Using the filter() Method

The `filter()` method can also be used to remove an item from an array by value. The `filter()` method takes a function as an argument and returns a new array containing only the items for which the function returns `true`.

For example, if you have an array `var arr = [1,2,3,4,5]` and you want to remove the item with value `3`, you would use the `filter()` method like this: 

```
arr = arr.filter(function(item){
  return item !== 3;
});
```

This will return a new array with only the items that are not equal to `3`. The result will be an array with four items: `[1,2,4,5]`.

##Using the indexOf() Method

The `indexOf()` method can also be used to remove an item from an array by value. The `indexOf()` method takes a value as an argument and returns the index of the first occurrence of that value in the array.

For example, if you have an array `var arr = [1,2,3,4,5]` and you want to remove the item with value `3`, you would use the `indexOf()` method like this: 

```
var index = arr.indexOf(3);
arr.splice(index,1);
```

This will first find the index of the item with value `3` and then use the `splice()` method to remove it. The result will be an array with four items: `[1,2,4,5]`.

##Using the for Loop

The `for` loop can also be used to remove an item from an array by value. The `for` loop will iterate over the array and remove the item if its value matches the value you are looking for.

For example, if you have an array `var arr = [1,2,3,4,5]` and you want to remove the item with value `3`, you would use the `for` loop like this: 

```
for(var i=0; i < arr.length; i++){
  if(arr[i] === 3){
    arr.splice(i,1);
  }
}
```

This will iterate over the array and remove the item with value `3` when it is found. The result will be an array with four items: `[1,2,4,5]`.
