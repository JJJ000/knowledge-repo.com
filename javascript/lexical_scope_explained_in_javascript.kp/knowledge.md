---
title: How does lexical scope work?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Lexical scope in JavaScript is the availability of variables within nested functions based on the nesting level of the functions within the source code.
---

**Contents**

[TOC]

# Definition
Lexical scope in Javascript is the scope of a variable in which the variable is defined. It is determined by the position of the variable within the code and is not affected by the context in which the variable is used. 

# How it Works
In Javascript, the scope of a variable is determined by the position of the variable in the code. Variables declared within a function are only accessible within that function and are said to have local scope. Variables declared outside of a function are accessible throughout the entire code and are said to have global scope. 

# Example
For example, consider the following code: 

```
let x = 10; 

function myFunction() {
  let y = 5; 
  console.log(x + y); 
}

myFunction(); 
```

In this code, the variable x has global scope because it is declared outside of a function. The variable y has local scope because it is declared within the function myFunction(). 

# Benefits
Lexical scope allows for better organization of code and helps to avoid conflicts between variables with the same name but different scopes. It also makes code easier to read by making it clear where a variable is accessible.
