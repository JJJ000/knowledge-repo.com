---
title: Retrieve an individual object by its identifier from a collection of objects in angularjs
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: AngularJS provides the filter filter which can be used to get a specific object by id from an array of objects in JSON.
---

**Contents**

[TOC]

**Section 1: Understanding the Problem**

The problem is to get a specific object by its id from an array of objects in AngularJS in JSON.

**Section 2: Solution**

The solution is to use the `filter()` method in AngularJS to filter the array of objects and get the object with the required id.

**Section 3: Code Example**

The following code example shows how to use the `filter()` method to get a specific object by its id from an array of objects in AngularJS in JSON.

```javascript
var arrayOfObjects = [
    {
        id: 1,
        name: "John"
    },
    {
        id: 2,
        name: "Jane"
    },
    {
        id: 3,
        name: "Bob"
    }
];

var objectById = arrayOfObjects.filter(function(obj) {
    return obj.id === 2;
})[0];

console.log(objectById);
// Output: {id: 2, name: "Jane"}
```

**Section 4: Conclusion**

By using the `filter()` method in AngularJS, it is possible to get a specific object by its id from an array of objects in JSON.
