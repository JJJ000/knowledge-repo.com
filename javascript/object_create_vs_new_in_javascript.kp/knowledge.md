---
title: Replacing "new" with "object.create"
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Object.create creates an object that has a specified prototype, and does not call a constructor function.
---

**Contents**

[TOC]

**Section 1: Overview**
Object.create is a method in JavaScript that creates a new object based on the prototype object passed as the first argument. It is a way to create an object without having to use the new keyword. This is useful when you want to create an object with a specific prototype or set of properties.

**Section 2: Benefits**
Object.create provides a clean and concise way to create an object without using the new keyword. It also allows for the creation of objects with a specific prototype, which can be useful when creating objects with different properties. Additionally, Object.create can be used to create objects that are not linked to the global object, which can be beneficial for code organization.

**Section 3: Drawbacks**
Object.create does not provide a way to set the constructor of the new object, which can be a limiting factor when creating objects. Additionally, Object.create does not provide a way to easily set the properties of the new object, which can make the process of creating an object more difficult.

**Section 4: Conclusion**
Object.create is a useful method for creating objects in JavaScript without having to use the new keyword. It provides a clean and concise way to create objects with specific prototypes, and can be beneficial for code organization. However, it does have some drawbacks, such as not providing a way to easily set the constructor and properties of the object.
