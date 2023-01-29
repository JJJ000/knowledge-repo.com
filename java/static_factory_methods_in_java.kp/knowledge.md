---
title: What are static methods used to create objects?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Static factory methods are methods that allow for the creation of objects without using the new keyword.
---

**Contents**

[TOC]

### Definition

Static factory methods are class methods that provide a way to create an object without using the `new` keyword. These methods can also provide additional features that are not available when using the `new` keyword, such as customizing the object based on parameters passed to the method.

### Advantages

Static factory methods provide several advantages over using the `new` keyword. They can be more concise and easier to read than using `new`, and they can also provide more flexibility in how an object is created. Additionally, they can be used to create objects that are immutable, which can be beneficial in certain situations.

### Disadvantages

The main disadvantage of static factory methods is that they can be difficult to discover, as they are not part of the public API. Additionally, they can be difficult to debug, as the code that creates the object is not visible in the code. Finally, they can also be difficult to maintain, as changes to the code that creates the object can require changes to the code that calls the method.
