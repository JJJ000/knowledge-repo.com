---
title: Unpacking tuples into parameters
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: In Python, tuples can be expanded into arguments using the * operator.
---

**Contents**

[TOC]

# Unpacking Tuples
Unpacking tuples is a way of splitting up the values stored in a tuple and assigning them to multiple variables. This can be done by assigning a tuple of variables on the left and a tuple of values on the right of an equals sign. 

# Syntax
The syntax for unpacking tuples is as follows: 
```
(variable1, variable2, ...) = (value1, value2, ...)
```

# Examples
Here are a few examples of unpacking tuples: 
```
# Assign the values of a tuple to individual variables
(x, y, z) = (1, 2, 3)
print(x) # 1
print(y) # 2
print(z) # 3

# Unpack a tuple in a for loop
tup = (1, 2, 3)
for i in tup:
    print(i)
# 1
# 2
# 3

# Unpack a nested tuple
tup = ((1, 2), (3, 4))
for a, b in tup:
    print(a + b)
# 3
# 7
```

# Applications
Unpacking tuples can be useful when dealing with function arguments. For example, if a function takes in a tuple of three values and you want to pass it three separate variables, you can use unpacking to do so. 

```
def my_func(x, y, z):
    return x + y + z

tup = (1, 2, 3)
my_func(*tup) # 6
```
