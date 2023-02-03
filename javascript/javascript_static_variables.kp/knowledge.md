---
title: Variables that maintain their value across multiple function calls in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Static variables in JavaScript are variables that retain their values between function calls.
---

**Contents**

[TOC]

# Definition
A static variable in JavaScript is a variable that is declared with the `static` keyword and is accessible only within the scope of its class or function.

# Usage
Static variables are typically used to store information that is needed throughout the lifetime of the program. For example, a static variable can be used to keep track of the number of times a particular function has been called.

# Scope
A static variable is only accessible within the scope of the class or function in which it is declared. It is not visible outside that scope.

# Advantages
Static variables are useful because they allow a programmer to store data that is needed throughout the lifetime of the program, without having to declare it each time the program is run. Additionally, they can be used to store data that needs to remain constant, such as configuration settings.
