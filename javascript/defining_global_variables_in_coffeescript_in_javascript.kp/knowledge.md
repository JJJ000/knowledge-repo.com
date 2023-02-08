---
title: What is the syntax for declaring global variables in coffeescript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: In CoffeeScript, global variables can be defined using the `window` keyword.
---

**Contents**

[TOC]

# Section 1: Defining Global Variables in CoffeeScript 

In CoffeeScript, global variables are declared with the keyword `global`. For example, to declare a variable named `myGlobal` as a global variable, you would write the following:

```
global myGlobal
```

# Section 2: Accessing Global Variables in CoffeeScript

Once a global variable is declared, it can be accessed anywhere in the script. For example, to access the global variable `myGlobal` declared in the previous section, you would write the following:

```
console.log(myGlobal)
```

# Section 3: Compiling CoffeeScript to JavaScript

When compiling CoffeeScript to JavaScript, the global variables declared in the CoffeeScript code are converted to `window` variables in the JavaScript code. For example, the CoffeeScript code from Section 1 would be compiled to the following JavaScript code:

```
window.myGlobal;
```

# Section 4: Accessing Global Variables in JavaScript

Once a global variable is declared in CoffeeScript and compiled to JavaScript, it can be accessed anywhere in the script. For example, to access the global variable `myGlobal` declared in the previous section, you would write the following:

```
console.log(window.myGlobal);
```
