---
title: What is the reason that instanceof returns false for certain literals?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Instanceof returns false for some literals because it can only be used to check if an object is an instance of a class or a constructor.
---

**Contents**

[TOC]

# Primitive Literals

Primitive literals are values that are not objects, such as numbers, strings, and booleans. These values are immutable and cannot be changed. Since instanceof is used to check if an object is an instance of a certain class, primitive literals will always return false when checked with instanceof.

# Constructor Functions

In JavaScript, constructor functions are used to create objects. When a constructor function is used to create an object, the object will be an instance of the constructor function. Therefore, when instanceof is used to check if an object is an instance of a certain constructor function, it will return true. However, primitive literals are not objects, so instanceof will always return false when used with primitive literals.

# Native Objects

In JavaScript, there are native objects such as Array, Date, and Math. These objects are built-in and are not created with a constructor function. Since these objects are not created with a constructor function, instanceof will always return false when used with native objects.

# Wrapper Objects

In JavaScript, primitive literals can be wrapped in an object using wrapper objects. For example, when a string literal is wrapped in a String object, the object will be an instance of the String constructor function. Therefore, when instanceof is used to check if an object is an instance of a certain constructor function, it will return true. However, if instanceof is used to check if a primitive literal is an instance of a certain constructor function, it will always return false.
