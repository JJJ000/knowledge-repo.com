---
title: Determine if a number is a decimal or an integer
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the modulo operator (`%`) to check if a number is a whole number, as a whole number will have a remainder of 0 when divided by 1.
---

**Contents**

[TOC]

## Check if a Number is a Whole Number

To check if a number is a whole number, we can use the JavaScript `Number.isInteger()` method. This method returns `true` if the number passed as an argument is an integer, and `false` if it is not.

```javascript
Number.isInteger(4); // returns true
Number.isInteger(4.5); // returns false
```

## Check if a Number has a Decimal Place

To check if a number has a decimal place, we can use the JavaScript `Number.isInteger()` method. This method returns `false` if the number passed as an argument has a decimal place, and `true` if it does not.

```javascript
Number.isInteger(4); // returns true
Number.isInteger(4.5); // returns false
```

## Alternative Method

An alternative method for checking if a number has a decimal place is to use the modulo operator `%` to divide the number by `1`. If the result is `0`, then the number does not have a decimal place.

```javascript
4 % 1; // returns 0
4.5 % 1; // returns 0.5
```
