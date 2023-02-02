---
title: What is the process for changing a decimal number to hexadecimal in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the built-in Number.prototype.toString() method, passing in a base of 16 to convert a decimal number to a hexadecimal string.
---

**Contents**

[TOC]

### Section 1: Understanding Conversion

The conversion from decimal to hexadecimal involves breaking down the decimal number into its component parts and then converting each part into its hexadecimal equivalent. Decimal numbers are base 10, meaning that each digit can range from 0 to 9. Hexadecimals, on the other hand, are base 16, so each digit can range from 0 to 15. 

### Section 2: Preparing the Conversion

Before beginning the conversion process, it is important to understand the value of each digit in the decimal number. To do this, start by breaking down the decimal number into its component parts. For example, if the decimal number is `123`, it can be broken down into `100`, `20`, and `3`. 

### Section 3: Converting Each Component

Once the decimal number has been broken down into its component parts, each part can be converted into its hexadecimal equivalent. To do this, start by dividing the part by 16. The remainder of the division is the first digit in the hexadecimal version of the part. The quotient of the division is then divided by 16, and the remainder of this division is the second digit in the hexadecimal version of the part. This process is repeated until the quotient is 0. 

For example, the decimal `100` can be divided by 16 to give a remainder of `4` and a quotient of `6`. The `6` can then be divided by 16 to give a remainder of `6` and a quotient of `0`. This gives us the hexadecimal equivalent of `64`. 

### Section 4: Putting it Together

Once each part has been converted into its hexadecimal equivalent, the parts can be combined to give the hexadecimal equivalent of the original decimal number. In the example above, the hexadecimal equivalent of `123` is `7B`.
