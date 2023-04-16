---
title: What are the distinctions between parseint() and number()?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: parseInt() parses a string and returns an integer, while Number() converts a value to a number.
---

**Contents**

[TOC]

### parseInt() 
parseInt() is a function that takes a string as an argument, and returns an integer. It parses the string until it finds a character that is not a number and stops.

### Number()
Number() is a function that takes any type of argument and returns a number. It will try to convert the argument to a number if it is not already one.

### Difference
The main difference between parseInt() and Number() is that parseInt() only works with strings, while Number() can work with any type of argument. Additionally, parseInt() only parses until it finds a character that is not a number, while Number() will try to convert the argument to a number.
