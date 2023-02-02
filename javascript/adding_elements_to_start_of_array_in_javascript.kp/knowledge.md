---
title: What is the syntax for prepending new elements to an array in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the unshift() method to add new array elements at the beginning of an array in JavaScript.
---

**Contents**

[TOC]

# Section 1: Using unshift()

The `unshift()` method is used to add new items to the beginning of an array and returns the new length of the array.

Syntax:
```
array.unshift(item1, item2, ..., itemX)
```

Example:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon", "Pineapple");

// ["Lemon", "Pineapple", "Banana", "Orange", "Apple", "Mango"]
```

# Section 2: Using spread operator

The spread operator (`...`) can be used to add elements to the beginning of an array.

Syntax:
```
[item1, item2, ..., itemX, ...array]
```

Example:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var newFruits = ["Lemon", "Pineapple", ...fruits];

// ["Lemon", "Pineapple", "Banana", "Orange", "Apple", "Mango"]
```

# Section 3: Using concat()

The `concat()` method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

Syntax:
```
array1.concat(array2, array3, ..., arrayX)
```

Example:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var newFruits = ["Lemon", "Pineapple"].concat(fruits);

// ["Lemon", "Pineapple", "Banana", "Orange", "Apple", "Mango"]
```

# Section 4: Using Array.from()

The `Array.from()` method creates a new, shallow-copied Array instance from an array-like or iterable object.

Syntax:
```
Array.from(arrayLikeObject, mapFunction, thisValue)
```

Example:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var newFruits = Array.from(fruits, (fruit) => `${fruit}s`);

// ["Bananas", "Oranges", "Apples", "Mangos"]
```
