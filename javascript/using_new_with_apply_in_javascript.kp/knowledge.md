---
title: Can the .apply() method be used with the 'new' operator?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: No, it is not possible to use the .apply() method with the `new` operator in JavaScript.
---

**Contents**

[TOC]

Yes, it is possible to use the .apply() method with the 'new' operator in Javascript.

Overview

The .apply() method allows a function to be invoked with a given this value and arguments provided as an array. The 'new' operator creates a new instance of a given constructor function with the provided arguments. Combining the two together allows for the invocation of a constructor function with a given this value and arguments provided as an array.

Syntax

The syntax for using the .apply() method with the 'new' operator is as follows: 

new constructorFn.apply(thisValue, [arg1, arg2, ...]);

Example

For example, the following code creates a new instance of the Person constructor function with the given this value and arguments: 

var person = new Person.apply(this, ['John', 'Smith']);

Conclusion

In conclusion, it is possible to use the .apply() method with the 'new' operator in Javascript. This allows for the invocation of a constructor function with a given this value and arguments provided as an array.
