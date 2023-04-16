---
title: What is the function of a self-executing function in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A self executing function in JavaScript is a function that executes automatically when it is defined.
---

**Contents**

[TOC]

**Definition**
A self executing function is a function that is declared and then immediately executed. It is also known as an Immediately Invoked Function Expression (IIFE).

**Syntax**
The syntax for a self executing function is as follows:

`(function() {
  // code goes here
})();`

**Purpose**
The purpose of a self executing function is to create a private scope, which prevents variables and functions from being accessed outside the function. This is useful for keeping variables and functions private and preventing them from being accessed by other scripts.

**Benefits**
The main benefit of using a self executing function is that it helps keep code organized and maintainable. It also helps to keep global namespace clean by avoiding the use of global variables. Additionally, it can be used to create closures, which can help with memory management.
