---
title: Comparing JavaScript passed by reference versus passed by value
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: JavaScript is passed by value, meaning that primitive values are copied and passed, while objects are passed by reference, meaning that the reference to the original object is passed.
---

**Contents**

[TOC]

# By Reference
In JavaScript, objects are passed by reference. This means that when an object is assigned to a variable, the variable holds a reference to the object, not the actual object itself. When the object is passed to a function, the function receives a reference to the object, not the object itself. This means that any changes made to the object within the function will affect the original object.

# By Value
In JavaScript, primitive values such as strings, numbers, booleans, and null are passed by value. This means that when a primitive value is assigned to a variable, the variable holds the actual value, not a reference to the value. When the value is passed to a function, the function receives the actual value, not a reference to the value. This means that any changes made to the value within the function will not affect the original value.
