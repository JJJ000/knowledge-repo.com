---
title: Forwarding arguments to another JavaScript function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Passing arguments to another function can be done by using the function`s parameters.
---

**Contents**

[TOC]

## Declaring the Function

The first step in passing arguments forward to another JavaScript function is to declare the function. This is done by writing the `function` keyword followed by the function name and parentheses, followed by a set of curly braces. Inside the curly braces, you can include any number of parameters that will be used as arguments for the function.

For example:

```
function myFunction(param1, param2, param3) {
  // code here
}
```

## Passing Arguments to the Function

Once the function has been declared, you can pass arguments to it when you call the function. This is done by writing the function name followed by parentheses, inside of which you can include any number of arguments.

For example:

```
myFunction(arg1, arg2, arg3);
```

## Using the Arguments Inside the Function

Once the arguments have been passed to the function, you can use them inside the function. This is done by referring to the arguments by their parameter names.

For example:

```
function myFunction(param1, param2, param3) {
  console.log(param1 + param2 + param3);
}
```

## Returning a Value

Finally, you can return a value from the function by using the `return` keyword. This will pass the value back to the calling code.

For example:

```
function myFunction(param1, param2, param3) {
  return param1 + param2 + param3;
}
```
