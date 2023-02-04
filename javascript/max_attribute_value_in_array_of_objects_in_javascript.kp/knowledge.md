---
title: Determining the highest value of a property in a collection of objects
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The max value of an attribute in an array of objects can be found using the Math.max() method.
---

**Contents**

[TOC]

**Section 1: Creating the Array of Objects**

In order to find the maximum value of an attribute in an array of objects, we first need to create the array. We can do this by declaring a variable and assigning it to an array of objects.

For example: 

```javascript
var arr = [
  {name: 'John', age: 21},
  {name: 'Jane', age: 23},
  {name: 'Bob', age: 19}
];
```

**Section 2: Finding the Max Value**

Now that the array of objects has been created, we can find the maximum value of the age attribute. To do this, we can use the `Math.max()` method, which takes an array of values as an argument and returns the maximum value.

We can use the `map()` method to extract the age values from the array of objects into a new array, which we can then pass as an argument to the `Math.max()` method.

For example: 

```javascript
var ages = arr.map(function(person) {
  return person.age;
});

var maxAge = Math.max.apply(null, ages);
```

**Section 3: Outputting the Max Value**

The `maxAge` variable now contains the maximum value of the age attribute. We can output this value to the console with the `console.log()` method.

For example:

```javascript
console.log(maxAge); // Outputs 23
```

**Section 4: Alternative Solutions**

In addition to the solution outlined above, there are other ways to find the maximum value of an attribute in an array of objects.

One alternative is to use the `reduce()` method, which takes a callback function as an argument and returns a single value.

For example:

```javascript
var maxAge = arr.reduce(function(max, person) {
  return (person.age > max) ? person.age : max;
}, 0);
```

Another alternative is to use the `sort()` method, which takes a comparison function as an argument and sorts the array in place.

For example:

```javascript
arr.sort(function(a, b) {
  return b.age - a.age;
});

var maxAge = arr[0].age;
```
