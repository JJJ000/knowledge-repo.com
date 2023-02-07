---
title: Explanation of assigning a value to a variable in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In JavaScript, the OR operator (||) is used to assign a value to a variable if the variable is either undefined or null.
---

**Contents**

[TOC]

##### Definition

JavaScript OR (||) is a logical operator that is used to check two conditions and returns a boolean value based on the result. It is a short-circuit operator, meaning that if the first condition is true, the second condition will not be evaluated.

##### Syntax

The syntax for the OR operator is: 
```
condition1 || condition2
```

##### Examples

For example, the following statement will return true if either condition1 or condition2 is true:
```
var x = 5;
var y = 10;

x == 5 || y == 10 // returns true
```

##### Variable Assignment

The OR operator can also be used for variable assignment. If the first variable is undefined or null, the second variable will be assigned to the variable. For example:

```
var x;
var y = 10;

x = x || y; // x is now equal to 10
```
