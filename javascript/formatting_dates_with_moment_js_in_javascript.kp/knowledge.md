---
title: Use moment.js to format a date
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Moment.js can be used to format dates in Javascript by using the .format() method.
---

**Contents**

[TOC]

# Formatting a Date
 Moment.js provides a number of methods to format a date. The most commonly used methods are as follows:

## Formatting a Date as a String
To format a date as a string, Moment.js provides the `format()` method. This method takes a string argument which specifies the format of the output string. For example, to format a date as "DD/MM/YYYY", the following code can be used:

```javascript
moment().format('DD/MM/YYYY')
```

## Formatting a Date as an Object
To format a date as an object, Moment.js provides the `toObject()` method. This method returns an object containing the date and time information. For example, to format a date as an object, the following code can be used:

```javascript
moment().toObject()
```

## Parsing a Date
To parse a date, Moment.js provides the `parse()` method. This method takes a string argument which specifies the format of the input string. For example, to parse a date in the format "DD/MM/YYYY", the following code can be used:

```javascript
moment().parse('DD/MM/YYYY')
```

## Outputting a Date
To output a date, Moment.js provides the `format()` and `toObject()` methods. The `format()` method takes a string argument which specifies the format of the output string. The `toObject()` method returns an object containing the date and time information. For example, to output a date as a string in the format "DD/MM/YYYY", the following code can be used:

```javascript
moment().format('DD/MM/YYYY')
```
