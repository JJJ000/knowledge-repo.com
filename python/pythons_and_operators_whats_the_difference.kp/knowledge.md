---
title: In python, when does the expression "i += x" have a distinct meaning from "i = I + x"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: There is no difference between `i += x` and `i = I + x` in Python.
---

**Contents**

[TOC]

Introduction
Python supports both the "+=" and "= +" operators for adding values to a variable in a convenient and concise way. However, there are some subtle differences between these two operators that programmers should be aware of. In this article, we'll explore those differences and when to use each operator.

Difference in Execution
The first difference between "+=" and "= +" is in how they execute. When you use "+=" to add a value to a variable, the addition operation is performed in-place, which means that the result is stored directly in the same memory location as the original variable. On the other hand, when you use "= +" to add a value to a variable, a new memory location is created to store the result, and then the original variable is assigned to that new memory location.

Example Code
To illustrate this difference, consider the following code examples:

```
# Using "+="
i = 0
i += 5
print(i)  # Output: 5

# Using "= +"
i = 0
i = i + 5
print(i)  # Output: 5
```

In both cases, the same value of 5 is added to the variable i. However, in the first example using "+=", the addition occurs in-place, which means that i is updated to contain the result directly. In the second example using "= +", a new memory location is created to store the result, and then i is assigned to that new memory location.

+= for Mutable Data Types
The second difference between "+=" and "= +" is specific to mutable data types, such as lists or dictionaries. When you use "+=" to add a new value to a mutable data type, the original data type is modified in-place to include the new value. On the other hand, when you use "= +" to add a new value to a mutable data type, a new data type is created to include the original values plus the new value, and then the original variable is assigned to that new data type.

Example Code
To illustrate this difference, consider the following code examples:

```
# Using "+=" with a list
my_list = [1, 2, 3]
my_list += [4]
print(my_list)  # Output: [1, 2, 3, 4]

# Using "= +" with a list
my_list = [1, 2, 3]
my_list = my_list + [4]
print(my_list)  # Output: [1, 2, 3, 4]
```

In both cases, the same value of 4 is added to the list. However, in the first example using "+=", the addition occurs in-place, which means that my_list is updated to include the new value directly. In the second example using "= +", a new list is created to include the original values plus the new value, and then my_list is assigned to that new list.

Conclusion
In conclusion, while both "+=" and "= +" operators can be used to add values to variables in Python, they have some differences in execution and behavior that programmers should be aware of. The key takeaway is that "+=" is useful for performing in-place addition to a variable or a mutable data type, while "= +" is useful for creating a new variable or data type that includes the original values plus the new value.
