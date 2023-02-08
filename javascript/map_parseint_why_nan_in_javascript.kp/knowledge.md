---
title: What is the reason that parseint returns nan when used with array#map?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: parseInt yields NaN with Array#map because it is not designed to parse non-string values.
---

**Contents**

[TOC]

## Parsing Strings

The `parseInt()` function is used to convert a string into an integer. When used without a radix, it assumes the string is in base 10. The `Array#map()` method calls the provided callback function once for every element in the array, and returns a new array with the results of each call. 

## Problems with Array#map

The main issue with using `parseInt()` with `Array#map()` is that the callback function will be called with the array element as its argument. If the element is not a string, `parseInt()` will not be able to convert it to an integer and will return `NaN`. 

## Solutions

One solution is to use the `Array#map()` method with a radix argument, which will tell `parseInt()` which base to use when parsing the string. Another solution is to use `Array#filter()` to filter out any non-string elements before calling `Array#map()`.
