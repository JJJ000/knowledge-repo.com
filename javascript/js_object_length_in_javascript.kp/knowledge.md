---
title: Size of a JavaScript object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The length of a JavaScript object is determined by the number of its own enumerable properties.
---

**Contents**

[TOC]

#Object Length

##Object.keys()
The Object.keys() method can be used to determine the length of a JavaScript object. This method returns an array of the object's keys, which can then be used to access the object's values. The length of the array will correspond to the number of properties in the object.

##Object.entries()
The Object.entries() method can also be used to determine the length of a JavaScript object. This method returns an array of the object's keys and values, which can then be used to access the object's properties. The length of the array will correspond to the number of properties in the object.

##For...in loop
The for...in loop can also be used to determine the length of a JavaScript object. This loop iterates over the object's properties and can be used to access each property's value. The number of iterations will correspond to the number of properties in the object.

##Object.getOwnPropertyNames()
The Object.getOwnPropertyNames() method can also be used to determine the length of a JavaScript object. This method returns an array of the object's property names, which can then be used to access the object's values. The length of the array will correspond to the number of properties in the object.
