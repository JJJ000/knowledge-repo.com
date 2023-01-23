---
title: What is the syntax for creating and initializing an array in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: To declare and initialize an array in Java, use the syntax `type[] arrayName = {value1, value2, ...};`.
---

**Contents**

[TOC]

### Declaration

In Java, an array is declared with the following syntax:

`type[] arrayName;`

Where `type` is the type of the array (e.g. `int`, `String`, etc.), and `arrayName` is the name of the array.

### Initialization

An array can be initialized in two ways:

1. Using the `new` keyword: 

`type[] arrayName = new type[size];`

Where `size` is the size of the array.

2. Using array literals:

`type[] arrayName = {element1, element2, ..., elementN};`

Where `element1`, `element2`, ..., `elementN` are the elements of the array.
