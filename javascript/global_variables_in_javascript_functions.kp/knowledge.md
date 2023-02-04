---
title: Declare a variable outside of a JavaScript function that can be accessed within the function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: A global variable in a JavaScript function can be declared using the `var` keyword outside of any function blocks.
---

**Contents**

[TOC]

### 1. Declaring Global Variable
A global variable can be declared in a JavaScript function using the `var` keyword. For example:

```js
function myFunction() {
  var globalVar = "This is a global variable";
}
```

### 2. Accessing Global Variable
A global variable declared in a JavaScript function can be accessed from anywhere in the code. For example:

```js
function myFunction() {
  var globalVar = "This is a global variable";
}

console.log(globalVar); // Outputs: "This is a global variable"
```

### 3. Modifying Global Variable
A global variable declared in a JavaScript function can also be modified from anywhere in the code. For example:

```js
function myFunction() {
  var globalVar = "This is a global variable";
}

globalVar = "This is a modified global variable";

console.log(globalVar); // Outputs: "This is a modified global variable"
```

### 4. Deleting Global Variable
A global variable declared in a JavaScript function can also be deleted from anywhere in the code. For example:

```js
function myFunction() {
  var globalVar = "This is a global variable";
}

delete globalVar;

console.log(globalVar); // Outputs: undefined
```
