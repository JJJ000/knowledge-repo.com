---
title: What is the syntax for performing a logical xor operation on two variables in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the `^` operator to get the logical XOR of two variables in Python.
---

**Contents**

[TOC]

# Using the Exclusive OR (XOR) Operator 
The XOR operator (^) in Python can be used to get the logical XOR of two variables. 

Syntax:
```
result = expression1 ^ expression2
```

Example:
```
x = True
y = False

result = x ^ y

print(result)
```

Output:
```
True
```

# Using the Logical Operators 
The logical operators in Python can also be used to get the logical XOR of two variables. 

Syntax:
```
result = (expression1 and not expression2) or (not expression1 and expression2)
```

Example:
```
x = True
y = False

result = (x and not y) or (not x and y)

print(result)
```

Output:
```
True
```
