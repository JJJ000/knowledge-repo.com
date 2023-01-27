---
title: Identifying an object property that has not been defined
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can detect an undefined object property in Javascript by using the `typeof` operator to check if the property is undefined.
---

**Contents**

[TOC]

`**` What is an Undefined Object Property?**
An undefined object property is a property of an object that has not been assigned a value. This can happen when the property has been declared but not initialized or when the property does not exist in the object.

`**` How to Detect an Undefined Object Property**
The simplest way to detect an undefined object property is to use the typeof operator. The typeof operator will return “undefined” if the property is not defined. 

For example, if we have an object called “myObject” with a property called “myProperty”, we can use the following code to check if the property is defined:

```javascript
if (typeof myObject.myProperty === "undefined") {
  // myProperty is undefined
}
```

`**` Other Ways to Detect an Undefined Object Property**
Another way to detect an undefined object property is to use the in operator. The in operator will return false if the property is not defined. 

For example, if we have an object called “myObject” with a property called “myProperty”, we can use the following code to check if the property is defined:

```javascript
if (!("myProperty" in myObject)) {
  // myProperty is undefined
}
```

`**` Conclusion**
In conclusion, an undefined object property is a property of an object that has not been assigned a value. To detect an undefined object property, you can use the typeof operator or the in operator.
