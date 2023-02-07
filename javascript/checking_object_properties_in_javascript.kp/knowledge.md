---
title: What is the process for determining if an object has a specific property in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the `in` operator to determine if an object has a given property.
---

**Contents**

[TOC]

# Using the `in` Operator

The `in` operator allows us to determine whether an object has a given property. It returns a boolean value (`true` or `false`) depending on whether the property exists in the object.

Syntax:
```
propertyName in objectName
```

Example:
```
const car = {
  make: 'Ford',
  model: 'Fiesta',
  year: 2020
};

console.log('make' in car); // returns true
console.log('mileage' in car); // returns false
```

# Using the `hasOwnProperty()` Method

The `hasOwnProperty()` method allows us to determine whether an object has a given property. It returns a boolean value (`true` or `false`) depending on whether the property exists in the object.

Syntax:
```
objectName.hasOwnProperty(propertyName)
```

Example:
```
const car = {
  make: 'Ford',
  model: 'Fiesta',
  year: 2020
};

console.log(car.hasOwnProperty('make')); // returns true
console.log(car.hasOwnProperty('mileage')); // returns false
```
