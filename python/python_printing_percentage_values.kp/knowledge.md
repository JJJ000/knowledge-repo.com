---
title: What is the method to display a percentage value in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the percent symbol (%) followed by the format specifier f to print a percentage value in Python.
---

**Contents**

[TOC]

## Introduction

Printing a percentage value in Python is a relatively straightforward task. In this tutorial, we'll take a look at two common ways of printing percentage values in Python.

## Method 1: Using the Percentage Symbol

The first and simplest method of printing a percentage value in Python is to use the percentage symbol (```%```) in the print statement. Let's take a look at an example:

```python
# Example 1
percentage = 75.0
print("The percentage is %", percentage)
```

In the above code, we have assigned the value ```75.0``` to the variable ```percentage```. We then use the percentage symbol in our print statement to insert the value of the ```percentage``` variable.

When we run the above code, we get the following output:

```
The percentage is % 75.0
```

As we can see, the percentage symbol is inserted into our string, and the value of the ```percentage``` variable is printed immediately afterwards.

## Method 2: Using String Formatting

Another way of printing a percentage value in Python is to use string formatting. Here's an example:

```python
# Example 2
percentage = 75.0
print("The percentage is {:.1f}%".format(percentage))
```

In this example, we're using the string formatting syntax to insert the value of the ```percentage``` variable into our string. The ```:.1f``` in the formatting string tells Python to format the value of the ```percentage``` variable with one decimal place.

When we run the above code, we get the following output:

```
The percentage is 75.0%
```

As we can see, the string formatting syntax has allowed us to include the percentage symbol in our string in a way that looks more natural.

## Conclusion

Printing a percentage value in Python can be done in a couple of ways. The simplest method is to use the percentage symbol in the print statement, while the more versatile method is to use string formatting. Both of these methods are easy to implement, and which one you choose will depend on your personal preference.
