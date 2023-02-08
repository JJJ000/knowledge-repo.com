---
title: Arrange the items in an array in alphabetical order based on one of its attributes
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the Array.prototype.sort() method and pass in a compare function to sort the array alphabetically on one property.
---

**Contents**

[TOC]

**Section 1 - Sort Function**

The sort() method can be used to sort an array alphabetically on one property. The syntax of the sort() method is as follows:

```
array.sort(function(a, b){
   //Compare a and b
   //Return value 
});
```

The function passed to sort() takes two parameters (a and b) which represent the two elements being compared within the array. The function should return a value that indicates the position of the elements in the sorted array.

**Section 2 - Return Values**

The return value of the sort() method should be a number indicating the position of the elements in the sorted array. The following values should be returned:

- If a is less than b, return a negative number
- If a is greater than b, return a positive number
- If a is equal to b, return 0

**Section 3 - Compare Property**

The sort() method can be used to sort an array alphabetically on one property by comparing the property values of each element in the array. For example, if we are sorting an array of objects by their name property, the sort() method can be used to compare the name property of each element in the array and return the appropriate value.

**Section 4 - Example Code**

Here is an example of how to use the sort() method to sort an array of objects alphabetically on one property:

```
let arr = [
   {name: 'John', age: 20},
   {name: 'Bob', age: 30},
   {name: 'Alice', age: 25}
];

arr.sort(function(a, b){
   let nameA = a.name.toUpperCase(); // ignore upper and lowercase
   let nameB = b.name.toUpperCase(); // ignore upper and lowercase
   if (nameA < nameB) {
     return -1;
   }
   if (nameA > nameB) {
     return 1;
   }
   // names must be equal
   return 0;
});

console.log(arr);
// Output: [{name: 'Alice', age: 25}, {name: 'Bob', age: 30}, {name: 'John', age: 20}]
```
