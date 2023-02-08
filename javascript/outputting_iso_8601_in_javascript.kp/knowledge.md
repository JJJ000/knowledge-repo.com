---
title: What is the syntax for producing an iso 8601 formatted string using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can output an ISO 8601 formatted string in JavaScript by using the toISOString() method.
---

**Contents**

[TOC]

## Using the Date Object

The `Date` object in JavaScript allows you to easily access the current date and time and format it in a variety of ways. To output an ISO 8601 formatted string, you can use the `toISOString()` method. This method will return a string in the ISO 8601 format, which is a standardized date and time format, and is commonly used for web APIs and other data exchange formats.

```
let date = new Date();
let isoString = date.toISOString();
// Outputs "2020-06-01T19:12:11.539Z"
```

## Using a Library

If you need more control over the formatting of your ISO 8601 string, or you need to output a date and time from the past or future, you can use a library like `date-fns`. This library provides a variety of methods for formatting and manipulating Date objects. To output an ISO 8601 string using this library, you can use the `formatISO` method.

```
import { formatISO } from 'date-fns';

let date = new Date();
let isoString = formatISO(date);
// Outputs "2020-06-01T19:12:11.539Z"
```

## Using String Manipulation

If you don't want to use a library and you need more control over the formatting, you can also use string manipulation. To do this, you will need to access the individual components of the Date object and format them into a string.

```
let date = new Date();
let isoString = `${date.getFullYear()}-${date.getMonth() + 1}-${date.getDate()}T${date.getHours()}:${date.getMinutes()}:${date.getSeconds()}.${date.getMilliseconds()}Z`;
// Outputs "2020-06-01T19:12:11.539Z"
```
