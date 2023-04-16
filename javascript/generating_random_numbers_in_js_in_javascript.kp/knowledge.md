---
title: Create a random number between two values using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Math.random() * (max - min) + min can be used to generate a random number between two numbers in JavaScript.
---

**Contents**

[TOC]

# Math.random()

Math.random() is a built-in JavaScript function that generates a random number between 0 (inclusive) and 1 (exclusive).

## Generating a Random Number Between Two Numbers

To generate a random number between two numbers, we can use the following formula:

`Math.random() * (max - min) + min`

Where `max` is the maximum number and `min` is the minimum number.

## Example

To generate a random number between 1 and 10:

`Math.random() * (10 - 1) + 1`

## Output

The output of the above formula will be a random number between 1 and 10.
