---
title: Removing items in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Objects can be deleted in JavaScript using the delete operator.
---

**Contents**

[TOC]

#### Deleting Properties

Deleting properties from an object can be done using the delete operator. It takes the object and the property name as its arguments and deletes the property from the object. The delete operator is used like this:

```javascript
delete objectName.propertyName;
```

#### Deleting Objects

Deleting an object is a bit different than deleting a property. To delete an object, you must use the JavaScript garbage collector. This is done by setting the object to null.

```javascript
objectName = null;
```

The garbage collector will eventually free up the memory associated with the object.

#### Deleting Array Elements

Deleting array elements is similar to deleting object properties. You can use the delete operator to delete a specific element from an array.

```javascript
delete arrayName[index];
```

This will remove the element from the array, but it will not re-index the array.

#### Deleting Array Elements with Splice

If you want to delete an element from an array and re-index the array, you can use the splice method. This takes two arguments: the index of the element to be deleted, and the number of elements to delete.

```javascript
arrayName.splice(index, 1);
```

This will delete the element at the specified index and re-index the array.
