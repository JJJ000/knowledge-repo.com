---
title: Javascript class.method versus class.prototype.method
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Class.method is a static method that is defined on the class itself, while Class.prototype.method is an instance method that is defined on the class`s prototype.
---

**Contents**

[TOC]

# Difference
Class.method creates a new method for all instances of a class, while Class.prototype.method creates a method for the prototype of the class.

# Class.method
Class.method is a function that is defined on the class object. It is created for all instances of the class and is accessible with the class name.

# Class.prototype.method
Class.prototype.method is a function that is defined on the prototype object of the class. It is only accessible from the prototype object and not from the class object. It is created for all instances of the class.

# Benefits
Class.method allows you to define a method that is available to all instances of the class, while Class.prototype.method allows you to define a method that is only available to the prototype object. This can be useful if you want to create a method that is only available to the prototype object and not to all instances of the class.
