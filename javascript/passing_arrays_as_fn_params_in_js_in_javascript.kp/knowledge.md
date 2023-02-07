---
title: Sending an array to a function as an argument in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can pass an array as a function parameter in Javascript by using the array`s name as the argument.
---

**Contents**

[TOC]

### Syntax

The syntax for passing an array as a function parameter in JavaScript is as follows:

```
functionName(arrayName);
```

### Example

For example, if we have an array called `myArray` and a function called `myFunction`, we can pass the array to the function like so:

```
myFunction(myArray);
```

### Parameters

The function can then access the array's elements by using the parameter name. For example, if the function takes a single parameter called `arr`, it can access the first element of the array like so:

```
var firstElement = arr[0];
```

### Return Value

The function can also return an array as its return value. For example, if the function takes two parameters, `arr1` and `arr2`, it could return the concatenation of the two arrays like so:

```
return arr1.concat(arr2);
```
