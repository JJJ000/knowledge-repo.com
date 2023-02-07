---
title: The modulo operator in JavaScript produces a negative result when used with negative numbers
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, JavaScript % (modulo) gives a negative result for negative numbers.
---

**Contents**

[TOC]

## Yes

Modulo in JavaScript returns the remainder when dividing two numbers. If the two numbers are both negative, the result will be negative.

For example, -20 % 7 equals -6.

## No

Modulo in JavaScript returns the remainder when dividing two numbers. If the two numbers are both positive, the result will be positive.

For example, 20 % 7 equals 6.
