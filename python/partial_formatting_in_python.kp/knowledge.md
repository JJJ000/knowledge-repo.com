---
title: Formatting of only a segment of a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Partial string formatting in Python allows inserting only certain variables in the specified string using curly braces and format() method with their respective indexes or names.
---

**Contents**

[TOC]

1. Introduction
Python provides various ways of formatting strings, i.e., representing text and values as a single string. One of the most commonly used methods for string formatting is the "format()" method, which takes one or more positional arguments and replaces them with their corresponding values. In some cases, we might want to replace only a part of a string with a specific value or variable. For such scenarios, Python provides partial string formatting.

2. What is partial string formatting?
Partial string formatting is a way of formatting only a part of a string, leaving the rest of the text as is. We can use curly braces {} to denote the position of the variable inside a string, as we do in the regular string formatting. However, instead of providing the value in the format method, we can use a placeholder value, which is used to replace only the specified part of the string.

3. How to use partial string formatting in Python?
Here's a simple example to illustrate the use of partial string formatting:

```
price = 10
product = "apple"

output = f"The price of {product} is ${price:.2f} per pound."
print(output)
```

In the above code snippet, we are using an "f-string" (formatted string literal), which allows us to embed expressions inside string literals. We specify the variables inside curly braces and use a colon to specify the format specifier. Here, we are using ".2f" to format the price variable to two decimal places. We then create the output string with the partial string formatting as "{price:.2f}".

Output:
```
The price of apple is $10.00 per pound.
```

4. Conclusion
In conclusion, partial string formatting in Python is a useful technique when we need to replace only specific parts of a string. We can use f-strings or the format() method to achieve partial string formatting, and we can use various format specifiers to control string formatting.
