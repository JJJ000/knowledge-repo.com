---
title: How does Python string formatting distinguish between %s and %d?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: %s is used for string formatting, while %d is used for integer formatting in Python.
---

**Contents**

[TOC]

## Introduction
String formatting is an efficient way of formatting strings in Python. It allows you to combine different data types and insert them into a string in a structured way. "%s" and "%d" are the two most commonly used string formatting operators in Python. This article explains the differences between %s and %d and why they are used.

## %s and %d explained
The %s operator is used to represent a string in a string formatting expression. It is used to represent any string object such as words, numbers or symbols.

On the other hand, the %d operator is used to represent an integer value. It only works with integer values and any attempt to pass a string value will result in an error. This means that %d can only be used with numerical data.

## Examples of %s and %d
Let’s take a look at an example to illustrate the difference between %s and %d.

```
customer_name = "John"
customer_age = 28
print("Hello %s, you are %d years old." % (customer_name, customer_age))
```

The output of the code is:

```
Hello John, you are 28 years old.
```

In this example, we used both %s and %d to format the string. We used %s to represent the name and %d to represent the age. This way, we were able to create a dynamic message that can be personalized for each customer.

## Conclusion
In summary, %s is used to represent a string while %d is used to represent an integer. It is essential to use the correct operator so that the string formatting expression functions correctly. Remember, any attempt to pass a string value to %d will fail, so it’s important to be mindful of the data types you are using.
