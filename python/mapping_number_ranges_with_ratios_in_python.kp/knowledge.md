---
title: Transform a set of numbers from one range to another, preserving the proportional relationship between them
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the formula `new\_value = ( (old\_value - old\_min) / (old\_max - old\_min) ) * (new\_max - new\_min) + new\_min` to convert a number from one range to another, while maintaining its ratio.
---

**Contents**

[TOC]

### Section 1: Introduction 

Converting a number range to another range, while maintaining the ratio, is a common task in mathematics and programming. In Python, this can be done using a few simple steps. This tutorial will discuss how to convert a number range to another range, while maintaining the ratio, in Python. 

### Section 2: The Formula

The formula for converting a number range to another range, while maintaining the ratio, is as follows: 

```
new_value = (((old_value - old_min) * (new_max - new_min)) / (old_max - old_min)) + new_min
```

In this formula, `old_value` is the value you want to convert, `old_min` and `old_max` are the minimum and maximum values of the original range, `new_min` and `new_max` are the minimum and maximum values of the new range, and `new_value` is the converted value.

### Section 3: Example

To illustrate how this formula works, let's use an example. Say we have a range of numbers from 0 to 10, and we want to convert this range to a range of numbers from 0 to 100. To do this, we can use the formula above.

First, we need to plug in the values for `old_value`, `old_min`, `old_max`, `new_min`, and `new_max`. In this example, `old_value` is 5, `old_min` is 0, `old_max` is 10, `new_min` is 0, and `new_max` is 100. 

Plugging these values into the formula, we get: 

```
new_value = (((5 - 0) * (100 - 0)) / (10 - 0)) + 0
```

Next, we can calculate the answer by solving the equation:

```
new_value = ((5 * 100) / 10) + 0
new_value = 50
```

So, the converted value is 50. 

### Section 4: Conclusion

In this tutorial, we discussed how to convert a number range to another range, while maintaining the ratio, in Python. We looked at the formula for doing this conversion, and then we used an example to illustrate how it works. With this knowledge, you should now be able to convert a number range to another range, while maintaining the ratio, in Python.
