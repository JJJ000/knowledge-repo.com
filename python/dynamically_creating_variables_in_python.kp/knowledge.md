---
title: What is the process for creating variables dynamically?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can dynamically create variables in Python by using dictionaries and assigning values to a key within the dictionary.
---

**Contents**

[TOC]

Create variables with a dictionary

One way to dynamically create variables in Python is by using dictionaries. In this method, we can use the key-value pairs of a dictionary to create variables. For example:

```
# create a dictionary with variables as keys and values
my_dict = {'x': 2, 'y': 3, 'z': 4} 

# create variables dynamically using dictionary keys
for var in my_dict:
    exec(f"{var}={my_dict[var]}")

# use the variables
print(x, y, z)  # output: 2 3 4
```

Using the `exec()` function, we can execute a string as Python code, which allows us to create variables dynamically. In the above code, we iterate over the keys of the dictionary `my_dict` and create variables with the same name as the key using string formatting.

Using `globals()` function

Another way to create variables dynamically is by using the `globals()` function, which returns a dictionary of the current global namespace. We can add key-value pairs to this dictionary to create variables. For example:

```
# create variables dynamically using globals()
globals()['a'] = 10
globals()['b'] = 20

# use the variables
print(a, b)  # output: 10 20
```

Using the `globals()` function, we add key-value pairs to the global namespace dictionary, effectively creating variables. We can then use these variables anywhere in the code as global variables.

Using the `setattr()` function

Another method to create variables dynamically is by using the built-in `setattr()` function, which allows us to set an attribute of an object dynamically. We can use this function to set attributes of the `globals()` object, effectively creating variables. For example:

```
# create variables dynamically using setattr()
setattr(globals(), 'c', 30)
setattr(globals(), 'd', 40)

# use the variables
print(c, d)  # output: 30 40
```

Using the `setattr()` function, we set attributes of the `globals()` object dynamically, effectively creating global variables. We can then use these variables anywhere in the code.
