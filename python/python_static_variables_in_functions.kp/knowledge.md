---
title: What are the Python analogs to static variables within a function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: In Python, static variables inside a function are created by declaring variables inside the function with the keyword `nonlocal`.
---

**Contents**

[TOC]

### Local Variables 

Python does not have static variables inside a function. However, the closest equivalent would be local variables. Local variables are variables declared inside a function and only accessible within that function. They are initialized each time the function is called, and the value is lost when the function returns. 

### Global Variables 

Another option is to use global variables. Global variables are variables declared outside a function and are accessible from anywhere in the code. They are not initialized each time the function is called, so the value is retained between calls. 

### Nonlocal Variables 

In Python 3, nonlocal variables were introduced. Nonlocal variables are variables declared inside a function but are accessible from outside the function. They are not initialized each time the function is called, so the value is retained between calls. 

### Closures 

Finally, closures are a way of creating a function that “remembers” the value of a variable from the scope in which it was defined. Closures are often used to create functions that behave like static variables inside a function.
