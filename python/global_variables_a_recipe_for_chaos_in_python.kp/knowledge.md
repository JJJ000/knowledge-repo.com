---
title: What makes global variables harmful?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Global variables can lead to confusion, errors, and unexpected behavior in code.
---

**Contents**

[TOC]

Global variables in Python are considered evil due to several reasons. These include the following:

### 1. Code Maintainability and Readability Issues

When a codebase relies excessively on global variables, it becomes difficult to read and maintain. Global variables make it difficult for developers to locate where a particular variable is used within the codebase, leading to inconsistent code quality.

### 2. Namespace Pollution

Using global variables can lead to namespace pollution in your code as it keeps reusing the variable name. Namespace pollution can cause unexpected behaviour when two parts of the code are accessing a global variable with the same name, and it can cause errors that are hard to debug.

### 3. Difficult to Debug

Global variables can be difficult to debug because they take in values from all over the codebase. It makes it challenging to keep tabs on how a particular variable's value changes over time. Debugging an issue in such cases can take longer, impacting the developer's productivity.

### 4. Unintended Consequences

Global variables can lead to unintended consequences when two different parts of the codebase access it. For instance, if you have two different pieces of code that use the same global variable, they can end up overwriting it or using outdated values, leading to unpredictable behaviour. 

In conclusion, to ensure maintainable code and good development best practices, it is better to minimize or avoid using global variables in Python. Instead, you can use arguments and return values to pass around data between functions, encapsulating them in classes and methods.
