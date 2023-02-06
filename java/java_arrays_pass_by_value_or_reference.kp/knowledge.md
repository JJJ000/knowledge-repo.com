---
title: In java, do arrays get passed by value or by reference?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Arrays are passed by reference in Java.
---

**Contents**

[TOC]

# Passed by Reference

In Java, arrays are passed by reference. This means that when a method is called with an array argument, the reference to the array is passed to the method. The method can then modify the array, but the changes will be reflected in the original array outside of the method.

# How It Works

When an array is passed as an argument to a method, a reference to the array is passed. This means that the method can modify the array, but the changes will be reflected in the original array outside of the method. For example, if an array is passed to a method, the method can modify the elements of the array, and the changes will be seen in the original array.

# Benefits

Passing arrays by reference has several benefits. It allows for more efficient memory usage, since the entire array does not need to be copied into the method's scope. It also allows for more efficient code, since the same array can be used in multiple methods. Finally, it allows for more flexibility, since the same array can be modified in multiple ways.

# Drawbacks

The main drawback of passing arrays by reference is that it can be difficult to keep track of the changes made to the array. It is possible for a method to modify an array in unexpected ways, which can lead to hard-to-debug errors. Additionally, passing arrays by reference can lead to unexpected results if the same array is modified in multiple methods.
