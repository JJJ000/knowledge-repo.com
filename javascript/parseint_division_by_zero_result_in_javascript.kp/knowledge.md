---
title: What is the result of using parseint(1/0, 19)?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: parseInt(1/0, 19) returns 18 because 1/0 evaluates to Infinity, which has a base 19 representation of 18.
---

**Contents**

[TOC]

# Introduction

The `parseInt` function in Javascript is used to convert strings into integers. It takes two parameters, the string to convert, and the base of the number (a number between 2 and 36). In this case, the string being passed is `1/0`, which is not a valid string.

# How parseInt works

When `parseInt` is passed a string that is not a valid number, it will return the value `NaN`, which stands for Not a Number. However, if the second parameter is set to a number between 2 and 36, the function will return a value based on the characters in the string, according to the specified base.

# Explanation

In this case, the second parameter is set to 19, so the function will attempt to convert the string `1/0` into an integer using base 19. Since base 19 only uses the characters 0-9 and A-I, the string `1/0` cannot be converted into a valid integer. As such, the function will return the highest valid integer it can find, which is 18.

# Conclusion

In summary, `parseInt(1/0, 19)` returns 18 because the string `1/0` cannot be converted into a valid integer using base 19. The function returns the highest valid integer it can find, which is 18.
