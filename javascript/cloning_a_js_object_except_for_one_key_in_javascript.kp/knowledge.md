---
title: What is the best way to duplicate a JavaScript object, excluding one key?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use Object.assign() to create a new object and pass the original object as the first argument, then pass an object containing the key to exclude as the second argument, with its value set to undefined.
---

**Contents**

[TOC]

**Section 1: Create a Copy of the Object**

The simplest way to clone a JavaScript object except for one key is to create a copy of the object. This can be done using the `Object.assign()` method. This method takes two arguments: the target object and the source object. The target object is the object to which the source object will be copied. The source object is the object from which the properties will be copied.

**Section 2: Remove the Desired Key**

Once the object has been copied, the desired key can be removed from the copy. This can be done using the `delete` operator. This operator takes the object and the key to be removed as its arguments.

**Section 3: Return the Cloned Object**

The cloned object can then be returned using the `return` statement. This statement takes the cloned object as its argument.

**Section 4: Example**

For example, consider the following object:

```
let obj = {
  name: 'John',
  age: 25,
  location: 'New York'
};
```

To clone this object except for the `age` key, we could use the following code:

```
let newObj = Object.assign({}, obj);
delete newObj.age;
return newObj;
```

The resulting object would be:

```
{
  name: 'John',
  location: 'New York'
}
```
