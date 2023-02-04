---
title: Create a hash map with an attribute value of the object as the index, using the object array as the data source
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Array.prototype.reduce() method to iterate over the array, creating a new object with the attribute value as the key and the object as the value.
---

**Contents**

[TOC]

**Section 1: Create Object Array**

```javascript
let objectArray = [
  {
    id: 1,
    name: 'John Doe'
  },
  {
    id: 2,
    name: 'Jane Doe'
  }
];
```

**Section 2: Create Hash Map**

```javascript
let hashMap = {};

for (let i = 0; i < objectArray.length; i++) {
  let obj = objectArray[i];
  hashMap[obj.id] = obj;
}
```

**Section 3: Accessing Values**

```javascript
// Accessing the first object in the array
console.log(hashMap[1]); // {id: 1, name: 'John Doe'}

// Accessing the second object in the array
console.log(hashMap[2]); // {id: 2, name: 'Jane Doe'}
```

**Section 4: Updating Values**

```javascript
// Updating the first object in the array
hashMap[1].name = 'John Smith';

// Accessing the first object in the array after update
console.log(hashMap[1]); // {id: 1, name: 'John Smith'}
```
