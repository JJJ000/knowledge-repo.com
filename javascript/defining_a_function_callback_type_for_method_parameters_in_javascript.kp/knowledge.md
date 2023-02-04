---
title: What is the specific type of a function callback that is being used as a parameter in a method?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The type for a function callback can be defined as a function type with its parameters and return type specified.
---

**Contents**

[TOC]

## Section 1: Defining Function Type

In Javascript, the type of a function callback is defined by the parameters and return type of the function. 

For example, a function callback with two parameters of type `string` and `number` and a return type of `boolean` would be defined as:

```javascript
function (string, number): boolean {
  // ...
}
```

## Section 2: Method Parameters

When defining a function callback for use in a method parameter, you need to specify the type of the function callback in the method signature.

For example, if a method takes a function callback as a parameter, the method signature would look something like this:

```javascript
function myMethod(callback: (string, number) => boolean): void {
  // ...
}
```

## Section 3: Using the Function

Once the function callback type has been defined in the method signature, the function can then be used in the method body.

For example, the method body might look something like this:

```javascript
function myMethod(callback: (string, number) => boolean): void {
  const result = callback('foo', 5);
  // ...
}
```

## Section 4: Passing in a Function

Finally, when calling the method, you need to pass in a function that matches the defined type.

For example, the function callback could be passed in as an anonymous function, like so:

```javascript
myMethod((str, num) => {
  return str.length > num;
});
```
