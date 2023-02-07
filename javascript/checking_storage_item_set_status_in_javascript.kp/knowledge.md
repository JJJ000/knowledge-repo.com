---
title: What is the process for determining if a storage item has been set?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can check if a Storage item is set by using the `getItem()` method and checking if the result is null or not.
---

**Contents**

[TOC]

# Section 1: Using the 'in' Operator
The 'in' operator is used to check if a property is present in an object. It is used to check if the specified property is in the object or its prototype chain.

Syntax: 
```
propertyName in objectName
```

Example:
```
let storage = {
  item1: 'value1',
  item2: 'value2'
};

console.log('item1' in storage); // true
console.log('item3' in storage); // false
```

# Section 2: Using the 'hasOwnProperty' Method
The 'hasOwnProperty' method is used to check if an object has a specified property as its own property (not inherited from its prototype chain).

Syntax: 
```
objectName.hasOwnProperty(propertyName)
```

Example:
```
let storage = {
  item1: 'value1',
  item2: 'value2'
};

console.log(storage.hasOwnProperty('item1')); // true
console.log(storage.hasOwnProperty('item3')); // false
```

# Section 3: Using the 'typeof' Operator
The 'typeof' operator is used to check the type of a variable or an expression. It can also be used to check if a property is set in an object.

Syntax: 
```
typeof objectName[propertyName]
```

Example:
```
let storage = {
  item1: 'value1',
  item2: 'value2'
};

console.log(typeof storage.item1); // string
console.log(typeof storage.item3); // undefined
```

# Section 4: Using the 'undefined' Comparison
The 'undefined' comparison is used to check if a variable or a property is undefined.

Syntax:
```
variableName === undefined
```

Example:
```
let storage = {
  item1: 'value1',
  item2: 'value2'
};

console.log(storage.item1 === undefined); // false
console.log(storage.item3 === undefined); // true
```
