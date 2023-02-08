---
title: What is the JavaScript equivalent of displaying the contents of a variable like php's var_dump or print_r?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: In Javascript, the equivalent of var\_dump or print\_r in PHP is console.log().
---

**Contents**

[TOC]

## console.log

The most basic equivalent of `var_dump` or `print_r` in JavaScript is `console.log`.

`console.log` will print out the value of a variable or expression to the console. This can be useful for debugging and inspecting values.

## JSON.stringify

Another way to inspect the contents of an object is to use `JSON.stringify`. This will convert the object into a string representation that can be logged to the console.

`JSON.stringify` will recursively traverse the object and convert it into a string. This can be useful to inspect the contents of a complex object.

## console.table

`console.table` is another way to inspect the contents of an object. It will display the contents of an object in a tabular format, making it easier to inspect the contents of an object.

## console.dir

`console.dir` is a way to inspect the contents of an object in a hierarchical format. This can be useful to quickly inspect the contents of an object and see how the object is structured.
