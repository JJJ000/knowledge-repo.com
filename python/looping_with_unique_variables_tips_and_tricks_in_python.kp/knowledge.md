---
title: In a loop, what is the process for generating varied variable names?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can concatenate a string with a loop counter or use a dictionary to create dynamic variable names in Python.
---

**Contents**

[TOC]

Section 1: Understanding the Problem

In Python, we sometimes need to create different variable names while in a loop. For example, if we are looping through a list of numbers and want to create individual variables for each number, we would need to name them differently. However, Python does not allow us to simply concatenate a loop variable with a string to create a unique variable name. So, how can we create different variable names while in a loop in Python?

Section 2: Using Dictionaries

One solution to this problem is to use a dictionary. We can define a dictionary outside of the loop and then add new key-value pairs to it during the loop. The keys would be the unique variable names we want to create, and the values would be the corresponding values of each iteration. Here is an example:

```
my_dict = {}

for i in range(5):
    var_name = "var_" + str(i)
    my_dict[var_name] = i

print(my_dict)
```

This would output:

```
{'var_0': 0, 'var_1': 1, 'var_2': 2, 'var_3': 3, 'var_4': 4}
```

Section 3: Using Lists

Another solution is to use a list. We can define an empty list outside of the loop and then append new elements to it during the loop. Each element can be a tuple containing the unique variable name and the corresponding value. Here is an example:

```
my_list = []

for i in range(5):
    var_name = "var_" + str(i)
    my_list.append((var_name, i))

print(my_list)
```

This would output:

```
[('var_0', 0), ('var_1', 1), ('var_2', 2), ('var_3', 3), ('var_4', 4)]
```

Section 4: Conclusion

In conclusion, there are multiple ways to create different variable names while in a loop in Python. One way is to use a dictionary and add new key-value pairs to it during the loop. Another way is to use a list and append new elements to it, with each element containing the unique variable name and corresponding value. Depending on the specific use case, one method may be more appropriate or efficient than the other.
