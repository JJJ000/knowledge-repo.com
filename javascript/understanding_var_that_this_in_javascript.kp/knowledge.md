---
title: What does 'var that = this;' refer to in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: `var that = this;` is used to store a reference to the current context, so that it can be used later in the code.
---

**Contents**

[TOC]

#### Definition

'var that = this;' is a JavaScript expression that assigns the value of the keyword 'this' to a variable named 'that'. 

#### Usage

The expression 'var that = this;' is typically used to store the value of 'this' in a variable so that it can be used in a different context. For example, if a method is called from an object, 'this' will refer to the object. However, if the method is called from a different context, 'this' will refer to something else. By storing the value of 'this' in a variable, the original context can be preserved.

#### Example

Consider the following example:

```javascript
var obj = {
  name: "John",
  sayName: function() {
    console.log(this.name);
  }
};

obj.sayName(); // prints "John"

// call sayName from a different context
var sayName = obj.sayName;
sayName(); // prints undefined

// use 'var that = this;' to preserve the original context
var obj = {
  name: "John",
  sayName: function() {
    var that = this;
    console.log(that.name);
  }
};

var sayName = obj.sayName;
sayName(); // prints "John"
```

In this example, the expression 'var that = this;' is used to preserve the value of 'this' within the sayName method, even when it is called from a different context.
