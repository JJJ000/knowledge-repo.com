---
title: How to convert an object {} to an array [] of key-value pairs using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Object.entries() method to convert an Object {} to an Array [] of key-value pairs in JavaScript.
---

**Contents**

[TOC]

**Section 1: Using Object.entries()**

The Object.entries() method can be used to convert an Object to an Array of key-value pairs. The syntax for this method is as follows:

```
Object.entries(object)
```

This method returns an array of key-value pairs for the given object.

**Section 2: Using Object.keys() and Object.values()**

The Object.keys() and Object.values() methods can be used to convert an Object to an Array of key-value pairs. The syntax for these methods is as follows:

```
Object.keys(object)
Object.values(object)
```

These methods return an array of the keys and values of the given object, respectively. We can then use the Array.map() method to combine the two arrays into a single array of key-value pairs.

**Section 3: Using for…in Loop**

The for…in loop can be used to iterate over the properties of an Object and convert them to an Array of key-value pairs. The syntax for this loop is as follows:

```
for (let key in object) {
    // code
}
```

Within the loop, we can access the key and value of each property and push them to an array.

**Section 4: Using Object.assign()**

The Object.assign() method can be used to convert an Object to an Array of key-value pairs. The syntax for this method is as follows:

```
Object.assign([target], object)
```

This method copies all enumerable own properties from the given object to the target array. The target array is then returned with the key-value pairs of the object.
