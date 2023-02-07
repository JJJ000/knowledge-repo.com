---
title: Describe the syntax for an encapsulated anonymous function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: An encapsulated anonymous function is a self-contained function that does not have a name and is declared and immediately invoked in one statement.
---

**Contents**

[TOC]

#### Definition
An encapsulated anonymous function is a function which is declared without a name and is immediately invoked. It is also known as an Immediately Invoked Function Expression (IIFE).

#### Syntax
The syntax for an encapsulated anonymous function in Javascript is as follows:

```
(function(){
  // Function body
})();
```

#### Benefits
The main benefit of using an encapsulated anonymous function is that it helps to create a local scope for variables declared within the function. This prevents the variables from being accessed from outside the function and therefore helps to protect the data. It also helps to avoid polluting the global namespace.

#### Example
An example of an encapsulated anonymous function in Javascript is as follows:

```
(function(){
  var x = 10;
  console.log(x);
})();
```
In this example, the variable x is declared within the function and is not accessible outside of it.
