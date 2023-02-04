---
title: What is the syntax for passing arguments to an addeventlistener listener function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Arguments can be passed to the addEventListener listener function by using an anonymous function as the second parameter.
---

**Contents**

[TOC]

### Section 1: Assignment of the Listener Function

The first step to passing arguments to an `addEventListener` listener function is to assign the listener function to a variable. This allows the function to be called later on with arguments. 

For example:

```javascript
var listenerFunction = function(event) {
    // Do something with the event
};
```

### Section 2: Adding the Listener

Once the listener function is assigned to a variable, it can be added as a listener to an element using the `addEventListener` method:

```javascript
element.addEventListener('click', listenerFunction);
```

### Section 3: Passing Arguments

To pass arguments to the listener function, the `bind` method can be used on the listener function. This will create a new function with the arguments bound to it. This new function can then be used as the listener:

```javascript
element.addEventListener('click', listenerFunction.bind(null, arg1, arg2));
```

### Section 4: Accessing the Arguments 

Within the listener function, the arguments can be accessed using the `arguments` keyword: 

```javascript
var listenerFunction = function(event) {
    var arg1 = arguments[0];
    var arg2 = arguments[1];
    // Do something with arg1 and arg2
};
```
